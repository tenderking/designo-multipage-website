<template>
	<div class="card-container">
		<CardItem v-for="card in cards" :key="card.id" :imgUrl="card.imgUrl" :title="card.title" :body="card.body" />
	</div>
</template>
<script setup lang="ts">
interface Card {
	id: number;
	imgUrl: string;
	title: string;
	body: string;
}
defineProps({
	cards: {
		type: Array as PropType<Card[]>,
		required: true,
	},
})
</script>
<style scoped>
.card-container {
	display: grid;
	grid-template-columns: repeat(auto-fit, minmax(275px, 1fr));
	justify-items: center;
	gap: 2rem;
}

@media (min-width: 768px) {
	.card-container {
		grid-template-columns: 1fr;
	}
}

@media screen and (min-width: 1024px) {
	.card-container {

		grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
	}
}
</style>