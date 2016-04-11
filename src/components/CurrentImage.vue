<template>
	<img src="./assets/background.jpg" class="responsive-image">
</template>

<script>
	export default {
		ready() {
			console.log(this.imageSrc)
		},
		props: ['imageSrc']
	}
</script>