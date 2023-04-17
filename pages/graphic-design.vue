<template>
  <NuxtLayout>
    <PageHero>
      <template #title>
        Graphic Design
      </template>
      <template #body>
        Great design makes you memorable. We deliver artwork that underscores your brand message and captures potential
        clients’ attention.
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
    imgUrl: '/assets/graphic-design/desktop/image-change.jpg',
    title: 'Tim Brown',
    body: 'A book cover designed for Tim Brown’s new release, ‘Change’',
  },
  {
    id: 2,
    imgUrl: '/assets/graphic-design/desktop/image-boxed-water.jpg',
    title: 'Boxed Water',
    body: 'A simple packaging concept made for Boxed Water',
  },
  {
    id: 3,
    imgUrl: '/assets/graphic-design/desktop/image-science.jpg',
    title: 'Science!',
    body: 'A poster made in collaboration with the Federal Art Project',
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
    title: 'App Design',
    destination: '/app-design',
    imgUrl: {
      mobile: '/assets/home/mobile/image-app-design.jpg',
      tablet: '/assets/home/tablet/image-app-design.jpg',
      desktop: '/assets/home/desktop/image-app-design.jpg',
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