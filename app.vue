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

h1 {
	font-size: 48px;
	font-weight: 500;
	line-height: 48px;
}

h2 {
	font-size: 40px;
	font-family: "Jost";
	font-weight: 500;
	line-height: 48px;
	letter-spacing: 2px;
}

h3 {
	font-size: 20px;
	font-family: "Jost";
	font-weight: 500;
	line-height: 26px;
	letter-spacing: 5px;
	text-transform: uppercase;
}
</style>
