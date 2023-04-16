<template>
	<div class="cta-container">
		<h2 class="h2">
			<slot name="title" />
		</h2>
		<p class="body">
			<slot name="body" />
		</p>
		<ButtonBase class="primary-btn">
			<slot name="button" />
		</ButtonBase>

	</div>
</template>
<style scoped>
.cta-container {
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	gap: 2rem;
	padding: 2rem;
	background-color: var(--color-primary-peach);
	max-width: var(--max-width);
	width: calc(100% - 4rem);
	margin: 2rem auto;
	border-radius: 15px;
	color: var(--color-primary-white);
	text-align: center;
}
</style>