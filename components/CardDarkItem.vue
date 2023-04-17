<template>
	<NuxtLink class="card-container" :to="destination">
		<h2 class="h2">
			<slot />
		</h2>
		<div class=" a-view-project">
			<span class="">
				view project
			</span>
			<i>
				<svg width="7" height="10" xmlns="http://www.w3.org/2000/svg">
					<path d="M1 1l4 4-4 4" stroke="#E7816B" stroke-width="2" fill="none" fill-rule="evenodd" />
				</svg>
			</i>
		</div>
		<!-- use picture for different img sizes mobile, desktop, tablet -->
		<picture>
			<source media="(min-width: 768px)" :srcset="imgUrl.desktop" />
			<source media="(min-width: 1440px)" :srcset="imgUrl.tablet" />
			<img :src="imgUrl.mobile" :alt="title" />

		</picture>

	</NuxtLink>
</template>
<script setup lang="ts">
// create a type for props
interface ImgUrl {
	mobile: string;
	tablet: string;
	desktop: string;
}

defineProps({
	destination: {
		type: String,
		required: true,
	},
	imgUrl: {
		type: Object as PropType<ImgUrl>,
		required: true,
	},
	title: {
		type: String,
		required: true,
	},
})
</script>

<style scoped>
.card-container {
	/* background-color: var(--color-primary-white); */
	display: flex;
	text-align: center;
	flex-direction: column;
	justify-content: center;
	align-items: center;

	padding-block: 5.625rem;

	position: relative;


	border-radius: 15px;
	color: var(--color-primary-white);
	isolation: isolate;
	overflow: hidden;
}

.card-container:hover::after {
	/* background transparent overlay */
	content: '';
	position: absolute;
	inset: 0;
	background-color: var(--color-primary-peach);
	opacity: 0.65;
	z-index: -1;

}



img {
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	z-index: -1;
	min-height: fit-content;
}

@media screen and (min-width: 768px) {


	.card-container {
		padding-block: 3.375rem;
	}
}

@media screen and (min-width: 1024px) {
	.card-container {
		padding-block: 5.625rem;
	}
}
</style>