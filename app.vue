<template>
	<div>
		<TheNavBar />
		<NuxtPage />
	</div>
</template>
<style>
@import url('https://fonts.googleapis.com/css2?family=Jost:wght@400;500&display=swap');

:root {
	--color-primary-peach: hsla(11, 72.1%, 66.3%, 1);
	--color-primary-black: hsla(270, 3.4%, 11.4%, 1);
	--color-primary-white: hsla(0, 0%, 100%, 1);
	--color-secondary-peach: hsla(11, 100%, 80.4%, 1);
	--color-secondary-dark-grey: hsla(264, 4.9%, 20.2%, 1);
	--color-secondary-light-grey: hsla(210, 16.7%, 95.3%, 0.858);
	--color-secondary-light-peach: hsla(14, 76%, 97%, 1);

	--max-width: 1112px;
	--screen-md: 768px;
}

* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}




#__nuxt {
	font-size: 16px;

	font-family: "Jost";
	font-weight: 400;
	font-style: normal;
	line-height: 26px;
	text-decoration: none;
	text-transform: none;

}

li,
a {
	font-family: "Jost";
	font-weight: 500;
	letter-spacing: 5px;
	text-transform: uppercase;
	text-decoration: none;
	color: inherit;
}


.h1 {
	font-family: Jost;
	font-size: 2rem;
	/* 32px */
	font-weight: 500;
	line-height: 36px;
	padding-bottom: 1rem;
	max-width: 20ch;
}

.h2 {
	font-family: Jost;
	font-size: 1.75rem;
	/* 28px */
	font-weight: 500;
	line-height: 36px;
	letter-spacing: 1.4px;
}

.h3 {
	font-family: Jost;
	font-size: 1.25rem;
	/* 20px */
	font-weight: 500;
	line-height: 26px;
	letter-spacing: 5px;
}

.body {
	max-width: 45ch;
}


.a-nav {
	font-family: Jost;
	font-size: 0.875rem;
	/* 14px */
	font-weight: 400;
	line-height: 14px;
	letter-spacing: 2px;
}

.a-view-btn {
	font-family: Jost;
	font-size: 0.9375rem;
	/* 15px */
	font-weight: 500;
	text-transform: uppercase;
	letter-spacing: 5px;
}

.a-cta-btn {
	font-family: Jost;
	font-size: 0.9375rem;
	/* 15px */
	font-weight: 500;
	text-transform: uppercase;
	letter-spacing: 1px;
}

.card-wrapper {
	display: grid;
	grid-template-columns: repeat(1, 1fr);
	grid-gap: 2rem;
	padding: 2rem 1rem;
}

@media screen and (min-width: 768px) {
	.card-wrapper {
		max-width: var(--max-width);
		width: calc(100% - 4rem);
		margin: 2rem auto;
		border-radius: 15px;

		padding: 0;
	}
}







/* desktop first card spans to rows  */
@media screen and (min-width: 1024px) {
	.card-wrapper {
		grid-template-columns: repeat(2, 1fr);
		grid-template-rows: repeat(2, 1fr);
		grid-gap: 2rem;
	}

}

@media screen and (min-width: 768px) {
	.h1 {
		font-family: Jost;
		font-size: 3rem;
		/* 48px */
		font-weight: 500;
		line-height: 48px;
		padding-bottom: 1rem;
	}

	.h2 {
		font-family: Jost;
		font-size: 2.5rem;
		/* 40px */
		font-weight: 500;
		line-height: 48px;
		letter-spacing: 2px;
	}

	.h3 {
		font-family: Jost;
		font-size: 1.25rem;
		/* 20px */
		font-weight: 500;
		text-transform: uppercase;
		line-height: 26px;
		letter-spacing: 5px;
	}

	.body {
		font-family: Jost;
		font-size: 1rem;
		/* 16px */
		font-weight: 400;
		line-height: 26px;
	}
}
</style>
