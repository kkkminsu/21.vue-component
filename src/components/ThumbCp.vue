<template>
	<li class="thumb">
		<img :src="img.src" :alt="img.title" class="w-100" @click="onChange">
	</li>
</template>

<script>
export default {
	name: 'ThumbCp',
	props: ['img'],
	methods: {
		onChange(e) {
			this.$emit('@change', { src: e.target.src, title: e.target.alt })
		}
	}
}
</script>

<style lang="scss" scoped>
.thumb {
	margin: 0 1%;
	cursor: pointer;
}
</style>