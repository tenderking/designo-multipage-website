<template>
	<div class="feature-item-wrapper">
		<img :src="imgUrl" :alt="title" class="img-phone" loading="lazy" width="200" height="200" />
		<div class="feature-text">
			<h3 class="h3 feature-title">
				<slot name="title" />
			</h3>
			<p class="body feature-description">
				<slot name="body" />
			</p>
		</div>
	</div>
</template>
<script setup>
defineProps({
	imgUrl: {
		type: String,
		required: true,
	},
	title: {
		type: String,
		required: true,
	},
});
</script>
<style scoped>
.feature-item-wrapper {
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	padding: 2rem;
}

.feature-text {
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
}

.feature-description {
	text-align: center;
	max-width: 36ch;
}

.feature-description,
.feature-title {
	margin-bottom: 2rem;
}

.feature-title {
	text-transform: uppercase;
}

.img-phone {
	position: relative;
	margin-bottom: 2rem;
	background-image: url("/assets/home/desktop/bg-pattern-hero-home.svg");
	background-repeat: no-repeat;
	background-position: center;
	background-size: cover;
	/* rotate: 180deg; */
}

/*gradient circle behind img  */

@media screen and (min-width: 768px) {
	.feature-item-wrapper {
		flex-direction: row;
		justify-content: space-between;
	}

	.feature-description {
		text-align: left;
		max-width: 50ch;
	}
}

@media screen and (min-width: 1024px) {
	.feature-item-wrapper {
		flex-direction: column;
	}

	.feature-description {
		text-align: center;
		max-width: 36ch;
	}
}
</style>
