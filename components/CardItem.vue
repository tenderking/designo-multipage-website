<template>
	<div class="card">

		<img :src="imgUrl" class="card__img" :alt="title" />

		<div class="card__content">
			<h3 class="card__title h3">{{ title }}</h3>
			<p class="card__body">{{ body }}</p>
		</div>

	</div>
</template>
<script setup lang="ts">
defineProps({
	imgUrl: {
		type: String,
		required: true,
	},
	title: {
		type: String,
		required: true,
	},
	body: {
		type: String,
		required: true,
	},
})
</script>
<style scoped>
.card {
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	margin: 0;
	border-radius: 15px;
	background-color: var(--color-primary-white);
	box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.1);
	overflow: hidden;
	background: var(--color-secondary-light-peach);
}

.card__img {
	width: 100%;
	margin: 0;
	padding: 0;
}

.card__content {

	padding: 2rem 1rem;
	margin: 0;
}



.card__title {
	color: var(--color-primary-peach);
	margin-bottom: 1rem;
	text-transform: uppercase;

}

/* .card__body {
	font-size: 1rem;
	font-weight: 400;
} */


@media screen and (min-width: 768px) {
	.card {
		flex-direction: row;

	}

	.card__img {
		width: 50%;
	}

	.card__content {
		width: 50%;

	}

}

@media screen and (min-width: 1024px) {
	.card {
		flex-direction: column;
		width: 350px;
	}

	.card__img {
		width: 100%;
	}

	.card__content {
		width: 100%;

	}

}
</style>
