<template>
	<f-container id="app">
		<component v-for="(component, index) in componentList"
			:key="index" :is="component" />
	</f-container>
</template>

<script>
import componentList from './mixin';

export default {
	data() {
		return {
			componentList
		}
	}
}
</script>

<style lang="scss">
#app {
	padding: 20px;
	h2 {
		margin: 20px 0;
	}
}
</style>

