<template>
  <main>
    <LandingHero />
    <div class="card-wrapper">
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

  .card-wrapper>*:nth-child(1) {
    /* grid-column: 1 / 3; */
    grid-row: 1 / 3;
  }
}
</style>
