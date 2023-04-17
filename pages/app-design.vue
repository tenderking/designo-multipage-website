<template>
  <NuxtLayout>
    <PageHero>
      <template #title>
        App Design
      </template>
      <template #body>
        Our mobile designs bring intuitive digital solutions to your customers right at their fingertips.
      </template>
    </PageHero>

    <CardContainer :cards="cards" class="wrapper" />
    <div class="card-wrapper">
      <CardDarkItem v-for="project in projects" :destination="project.destination" :imgUrl="project.imgUrl"
        :title="project.title">
        {{ project.title }}
      </CardDarkItem>
    </div>
  </NuxtLayout>
</template>
<script setup lang="ts">

const cards = [
  {
    id: 1,
    imgUrl: '/assets/app-design/desktop/image-airfilter.jpg',
    title: 'Airfilter',
    body: 'Solving the problem of poor indoor air quality by filtering the air',
  },
  {
    id: 2,
    imgUrl: '/assets/app-design/desktop/image-eyecam.jpg',
    title: 'Eyecam',
    body: 'Product that lets you edit your favorite photos and videos at any time',
  },
  {
    id: 3,
    imgUrl: '/assets/app-design/desktop/image-faceit.jpg',
    title: 'Faceit',
    body: 'Get to meet your favorite internet superstar with the faceit app',
  },
  {
    id: 4,
    imgUrl: '/assets/app-design/desktop/image-todo.jpg',
    title: 'Todo',
    body: 'A todo app that features cloud sync with light and dark mode',
  },
  {
    id: 5,
    imgUrl: '/assets/app-design/desktop/image-loopstudios.jpg',
    title: 'Loopstudios',
    body: 'A VR experience app made for Loopstudios',
  },
]
const projects = [
  {
    title: 'Web Design',
    destination: '/web-design',
    imgUrl: {
      mobile: '/assets/home/mobile/image-web-design.jpg',
      tablet: '/assets/home/tablet/image-web-design.jpg',
      desktop: '/assets/home/desktop/image-web-design-large.jpg',
    },
  },
  {
    title: 'Graphic Design',
    destination: '/graphic-design',
    imgUrl: {
      mobile: '/assets/home/mobile/image-graphic-design.jpg',
      tablet: '/assets/home/tablet/image-graphic-design.jpg',
      desktop: '/assets/home/desktop/image-graphic-design.jpg',
    },
  },
]

</script>
<style scoped>
.wrapper {
  max-width: var(--max-width);
  width: calc(100% - 4rem);
  margin: 2rem auto;
}
</style>

