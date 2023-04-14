<template>
	<div class="wrapper">
		<h2 class="h2">
			<slot />
		</h2>
		<NuxtLink class="a-view-project" :to="destination">
			<span class="">
				view project
			</span>
			<i>
				<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
					stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
					class="feather feather-arrow-right">
					<line x1="5" y1="12" x2="19" y2="12"></line>
					<polyline points="12 5 19 12 12 19"></polyline>
				</svg>

			</i>
		</NuxtLink>

		<img :src="imgUrl" alt="">
	</div>
</template>
<script setup lang="ts">

const props = defineProps({
	destination: {
		type: String,
		required: true,
	},
	imgUrl: {
		type: String,
		required: true,
	},
})
</script>

<style scoped>
.wrapper {
	/* background-color: var(--color-primary-white); */
	display: flex;
	text-align: center;
	/* flex-direction: column; */
	/* justify-content: center; */
	/* align-items: center; */
	/* padding: 2rem; */
	overflow: hidden;
	position: relative;


	border-radius: 15px;
	color: var(--color-primary-white);
	outline: solid;
	height: 250px;
}



img {
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	z-index: -1;
}
</style>