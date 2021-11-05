<template>
	<div class="app-wrapper">
		<ImgCp />
	</div>
</template>

<script>
import axios from 'axios'
import ImgCp from './components/ImgCp.vue'

export default {
	name: 'App',
	components: { ImgCp },
	beforeCreate() {
		console.log('beforeCreate')
	},
	beforeMount() {
		console.log('beforeMount')
	},
	async created() {
		console.log('Create')
		const { data } = await axios.get('/json/foods.json')
		console.log(data)
	}
}
</script>

<style lang="scss" scoped>
.app-wrapper {
	max-width: 400px;
	margin: 2em auto;
}
</style>