<template>
	<main>
		<slot name="default" />
		<CtaSection class="cta-section">
			<template #title>
				Let's talk about your project
			</template>
			<template #body>
				Ready to take it to the next level? Contact us today and find out how our expertise can help your business grow.
			</template>
			<template #button>
				Get in touch
			</template>
		</CtaSection>
	</main>
	<footer>
		<TheFooter />
	</footer>
</template>
<style scoped>
footer {
	background-color: var(--color-primary-black);
	padding-top: 6rem;
	margin-bottom: 0;
	margin: auto;
}

main {
	position: relative;
}

.cta-section {
	position: relative;
	top: 8rem;
	margin-top: -8rem;
}

/* desktop first card spans to rows  */
@media screen and (min-width: 1024px) {

	.cta-section {
		margin-top: -12rem;
	}

}
</style>