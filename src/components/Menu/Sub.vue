<template>
	<li
		@mouseenter="show"
		@mouseleave="hide">
		<a
			:href="link" :target="target"
			class="ms-menu-sub"
			:class="{
				'ms-menu-item-disabled': disabled,
				'select': isSelect,
				'active': isActive
			}">

			<i v-if="icon !== null" :class="icon"></i>
			<span class="text">{{ text }}</span>
			<i :class="`${$fabric.icon.right} ms-ChevronRight`"></i>
		</a>

		<f-menu
			ref="subMenu"
			:menu="subMenu"
			:size="computedSize"
		></f-menu>
	</li>
</template>

<script>
import mixin from './mixin';
import globalMxin from '../mixin';

export default {
	name: 'f-menu-sub-item',
	mixins: [mixin, globalMxin],
	methods: {
		show() {
			if (this.disabled) {
				return;
			}

			this.select();
			this.$refs.subMenu.show();
		},
		hide() {
			this.unSelect();
			this.$refs.subMenu.hide();
		}
	}
}
</script>

<style lang="scss">
a.ms-menu-sub {
	padding-left: 4px;
}
</style>

