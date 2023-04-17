<template>
	<div class="page-hero__wrapper">

		<h2 class="landing-text h2">
			<slot name="title" />
		</h2>

		<p class="landing-text body">
			<slot name="body" />
		</p>
		<picture>
			<source srcset="/assets/app-design/desktop/bg-pattern-intro-app.svg" media="(min-width: 768px)">

			<img src="/assets/home/desktop/bg-pattern-hero-home.svg" alt="background pattern" class="page-bg-shape">
		</picture>
	</div>
</template>
<style scoped>
.page-hero__wrapper {
	background-color: var(--color-primary-peach);
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	padding: 6rem 2rem;
	gap: 2rem;
	position: relative;
	overflow: hidden;
	text-align: center;
	color: var(--color-primary-white);

}

/* image to fit in page-hero__wrapper without overflowing */
.page-bg-shape {
	position: absolute;
	bottom: 0;
	right: 10px;
	width: 70%;
}


@media screen and (min-width: 768px) {
	.page-hero__wrapper {

		max-width: var(--max-width);
		width: calc(100% - 4rem);
		margin: 2rem auto;
		border-radius: 15px;
		padding-block: 4rem;

	}
}
</style>