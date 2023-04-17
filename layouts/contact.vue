<template>
	<main>
		<slot name="default" />

	</main>
	<footer>
		<TheFooter />
	</footer>
</template>
<style scoped>
footer {
	background-color: var(--color-primary-black);
	padding-top: 1rem;
	margin-bottom: 0;
}





/* desktop first card spans to rows  */
</style>