<template>
	<div class="wrapper">

		<div class="container">

			<h1 class="landing-text h1">
				Award-winning custom designs and digital branding solutions
			</h1>

			<p class="landing-text body">
				With over 10 years in the industry, we are experienced in creating fully responsive websites, app design,
				and engaging brand experiences. Find out more about our services.
			</p>

			<ButtonBase class="primary-btn">Learn More</ButtonBase>
		</div>

		<img class="img-phone" src="/assets/home/desktop/image-hero-phone.png" alt="landing page image">


	</div>
</template>
<style scoped>
.wrapper {
	background-color: var(--color-primary-peach);
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	padding: 2rem;
	/* position: relative; */
	overflow-y: hidden;
	height: 800px;
}

.img-phone {
	position: relative;
	left: 0;
	top: 0;
	object-fit: contain;
}

.container {
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	padding: 1rem;
}

.landing-text {
	color: var(--color-primary-white);
	text-align: center;
}

p.body {
	margin-bottom: 2rem;

}

button {
	margin-inline: auto;
}

@media screen and (min-width: var(--screen-md)) {
	.wrapper {
		flex-direction: row;
		justify-content: space-between;
		align-items: center;
		max-width: var(--max-width);
		width: calc(100% - 4rem);
		margin: 2rem auto;
		border-radius: 15px;
		height: 640px;
	}

	.container {
		flex-direction: column;
		justify-content: center;
		align-items: flex-start;
	}

	.landing-text {
		text-align: left;
	}

	button {
		margin-inline: 0;
	}
}
</style>