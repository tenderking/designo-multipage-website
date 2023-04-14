<template>
  <main>
    <LandingHero />
    <div class="wrapper">
      <CardDarkItem v-for="project in projects" :destination="project.destination" :imgUrl="project.imgUrl">
        {{ project.title }}
      </CardDarkItem>
    </div>
  </main>
</template>
<script setup lang="ts">
const projects = [
  {
    title: 'Web Design',
    destination: '/web-design',
    imgUrl: '/assets/home/mobile/image-web-design.jpg',
  },
  {
    title: 'Graphic Design',
    destination: '/graphic-design',
    imgUrl: '/assets/home/mobile/image-graphic-design.jpg',
  },
  {
    title: 'App Design',
    destination: '/app-design',
    imgUrl: '/assets/home/mobile/image-app-design.jpg',
  }
]

</script>
<style scoped>
.wrapper {
  display: grid;
  grid-template-columns: repeat(1, 1fr);
  grid-gap: 2rem;
  padding: 2rem 1rem;

}
</style>
