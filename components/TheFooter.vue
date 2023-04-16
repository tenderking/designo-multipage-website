<template>
	<div class="footer-container">
		<nav>
			<NuxtLink to="/">
				<img src="/assets/shared/desktop/logo-light.png" class="logo" />
			</NuxtLink>

			<ul class="menu">
				<li>
					<NuxtLink class="a-nav" to="/about">Our Company</NuxtLink>
				</li>
				<li>
					<NuxtLink class="a-nav" to="/locations">Locations</NuxtLink>
				</li>
				<li>
					<NuxtLink class="a-nav" to="/contact">Contact</NuxtLink>
				</li>
			</ul>
		</nav>
		<div class="contact-info__container">
			<div class="adress-wrapper">
				<p>Designo Central Office</p>
				<p> 3886 Wellington Street</p>
				<p>Toronto, Ontario M9C 3J5</p>
			</div>
			<div class="contact-info__wrapper">
				<p> Contact Us (Central Office)</p>
				<p> P : +1 253-863-8967</p>
				<p> M : contact@designo.co</p>
			</div>
			<div class="social-media__wrapper">
				<img src="/assets/shared/desktop/icon-facebook.svg" alt="facebook">
				<img src="/assets/shared/desktop/icon-twitter.svg" alt="twitter">
				<img src="/assets/shared/desktop/icon-instagram.svg" alt="instagram">
				<img src="/assets/shared/desktop/icon-pinterest.svg" alt="pinterest">
				<img src="/assets/shared/desktop/icon-youtube.svg" alt="youtube">
			</div>
		</div>
	</div>
</template>
<style scoped>
.footer-container {
	background-color: var(--color-primary-black);
	padding: 2rem 0;
	max-width: var(--max-width);
	width: calc(100% - 4rem);
	margin: auto;
	display: flex;
	flex-direction: column;
}

.logo {
	width: 202px;
	margin-bottom: 2rem;
}

nav {
	display: flex;
	flex-direction: column;
	align-items: center;
	color: var(--color-primary-white);
}

/* create a line under the logo */
nav::after {
	content: "";
	display: block;
	width: 100%;
	position: absolute;
	height: 1px;
	background-color: var(--color-primary-white);
	opacity: 0.2;
	margin-top: 3rem;

}

ul {
	list-style: none;
	display: flex;
	justify-content: space-between;
	flex-direction: column;
	align-items: center;
	gap: 2rem;

}

.contact-info__container {
	display: flex;
	flex-direction: column;
	justify-content: space-between;
	align-items: center;
	margin-top: 2rem;
	color: var(--color-secondary-light-grey);
	gap: 2rem;
	text-align: center;
}

.social-media__wrapper {
	display: flex;
	gap: 1rem;
}

@media screen and (min-width: 768px) {


	nav {
		flex-direction: row;
		justify-content: space-between;
		align-items: center;
	}

	.logo {
		margin-bottom: 0;
	}

	ul {
		flex-direction: row;
	}

	.contact-info__container {
		flex-direction: row;
		justify-content: space-between;
		align-items: center;
		text-align: left;
		padding-bottom: 2rem;
	}

	.adress-wrapper {
		margin-right: 2rem;
	}

	.contact-info__wrapper {
		margin-right: 2rem;
	}
}
</style>