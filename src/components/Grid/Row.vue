<template>
	<div class="ms-row">
		<slot></slot>
	</div>
</template>

<script>
export default {
	name: 'f-row',
	mounted() {
		const isWarning = this.$slots.default.filter(tabItem => {
			return tabItem.tag && (!tabItem.componentOptions || tabItem.componentOptions.tag !== 'f-col');
		})
			.length > 0;


		if (isWarning) {
			console.warn('The child of f-row component must be f-col component.')
		}
	}
}
</script>

<style lang="scss">
@import 'office-ui-fabric-core/src/sass/_References.scss';

.ms-row {
	display: block;
	width: 100%;
	@include ms-borderBox;
  @include ms-clearfix; 
}
</style>
