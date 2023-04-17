<template>
  <NuxtLayout>
    <PageHero>
      <template #title>
        Web Design
      </template>
      <template #body>
        We build websites that serve as powerful marketing tools and bring memorable brand experiences.
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
    imgUrl: '/assets/web-design/desktop/image-express.jpg',
    title: 'Express',
    body: 'A multi-carrier shipping website for ecommerce businesses',
  },
  {
    id: 2,
    imgUrl: '/assets/web-design/desktop/image-transfer.jpg',
    title: 'Transfer',
    body: 'Site for low-cost money transfers and sending money within seconds',
  },
  {
    id: 3,
    imgUrl: '/assets/web-design/desktop/image-photon.jpg',
    title: 'Photon',
    body: 'A state-of-the-art music player with high-resolution audio and DSP effects',
  },
  {
    id: 4,
    imgUrl: '/assets/web-design/desktop/image-builder.jpg',
    title: 'Builder',
    body: 'Connects users with local contractors based on their location',
  },
  {
    id: 5,
    imgUrl: '/assets/web-design/desktop/image-blogr.jpg',
    title: 'Blogr',
    body: 'Blogr is a platform for creating an online blog or publication',
  },
  {
    id: 6,
    imgUrl: '/assets/web-design/desktop/image-camp.jpg',
    title: 'Camp',
    body: 'Get expert training in coding, data, design, and digital marketing',
  },
]
const projects = [
  {
    title: 'App Design',
    destination: '/app-design',
    imgUrl: {
      mobile: '/assets/home/mobile/image-app-design.jpg',
      tablet: '/assets/home/tablet/image-app-design.jpg',
      desktop: '/assets/home/desktop/image-app-design.jpg',
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