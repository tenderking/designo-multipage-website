<template>
	<!-- Button base with can be used with slot for text and two types of classes for colors -->
	<button class="button-base a-cta-btn">
		<slot></slot>
	</button>
</template>

<style scoped>
.inverse-btn {
	--background-color: var(--color-primary-peach);
	--color: var(--color-primary-white);
}

.primary-btn {
	--background-color: var(--color-primary-white);
	--color: var(--color-primary-black);
}

.button-base {
	background-color: var(--background-color);
	color: var(--color);
	border: none;
	border-radius: 0.5rem;
	padding: 1rem 2rem;
	cursor: pointer;
	transition: all 0.2s ease-in-out;
	font-style: medium;
	font-size: 1rem;
	line-height: 22px;
	vertical-align: top;
	letter-spacing: 1px;
}

.button-base:hover {
	transform: translateY(-0.2rem);
	box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.2);
	background-color: var(--color-secondary-peach);
	color: var(--color-primary-white);
}
</style>