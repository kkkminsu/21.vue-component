<template>
	<div class="header-wrapper">
		<h1 class="logo">Hello {{ name }}</h1>
		<button @click="showAlert">눌러봐</button>
	</div>
</template>

<script>
export default {
	name: 'App',
	data() {
		return {
			name: 'Booldook'
		}
	},
	methods: {
		showAlert(e) {
			alert('Hello ' + this.name)
		}
	}
}
</script>

<style lang="scss">
.header-wrapper {
	text-align: center;
	h1.logo {
		color: red;
	}
}
</style>