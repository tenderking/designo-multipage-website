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
		<svg class="bg-shape" width="640" height="639" xmlns="http://www.w3.org/2000/svg">
			<defs>
				<linearGradient x1="0%" y1="50%" x2="100%" y2="50%" id="a">
					<stop stop-color="#5D0202" stop-opacity="0" offset="0%" />
					<stop stop-color="#5D0202" stop-opacity=".498" offset="100%" />
				</linearGradient>
			</defs>
			<circle fill="url(#a)" transform="matrix(0 -1 -1 0 640 640)" cx="320" cy="320" r="320" fill-rule="evenodd"
				opacity=".309" />
		</svg>
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
	position: relative;
	overflow: hidden;

}

.bg-shape {
	position: absolute;
	bottom: 0;
	right: 0;
}

.img-phone {
	position: relative;
	left: 0;
	margin: -10%;
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

@media screen and (min-width: 768px) {
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

	.img-phone {

		top: 40%;
	}

	.landing-text {
		text-align: left;
	}

	button {
		margin-inline: 0;
	}
}
</style>