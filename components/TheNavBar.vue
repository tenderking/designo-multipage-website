
<script setup lang="ts">
//use vue-use to toggle menu-toggle
import { useToggle } from '@vueuse/core'

const [isMenuOpen = false, toggleMenu] = useToggle()

</script>
<template>
  <nav>
    <NuxtLink to="/">
      <img src="/assets/shared/desktop/logo-dark.png" class="logo-dark" />
    </NuxtLink>
    <div class="menu-toggle" @click="toggleMenu()">
      <span></span>
      <span></span>
      <span></span>
    </div>
    <ul class="menu" :class="{ 'active': isMenuOpen }">
      <li>
        <NuxtLink class="a-nav" to="/about">Our Company</NuxtLink>
      </li>
      <li>
        <NuxtLink class="a-nav" to="/locations">Locations</NuxtLink>
      </li>
      <li>
        <NuxtLink class="a-nav" to="/contact">Contact</NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: relative;
  background-color: var(--color-primary-white);
  padding: 1rem;
}

.logo-dark {
  width: 202px;
}

.menu li {
  list-style: none;
}

.menu-toggle {
  display: block;
}

.menu {
  display: none;
  position: absolute;
  top: 100%;
  left: 0;
  width: 100%;
  text-align: center;
  padding: 20px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
  z-index: 10;
  background-color: var(--color-primary-black);
  color: var(--color-primary-white);
}

.menu.active {
  display: flex;
  flex-direction: column;
}


.menu-toggle span {
  display: block;
  height: 2px;
  width: 25px;
  margin-bottom: 5px;
  background-color: #333;
}

@media screen and (min-width: 768px) {
  nav {
    max-width: var(--max-width);
    margin: auto;
  }

  .menu-toggle {
    display: none;
  }

  .menu {
    position: static;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    margin: 0;
    box-shadow: none;
    padding: 0;
    background-color: transparent;
    color: var(--color-primary-black);
  }

  .menu li {
    margin-left: 20px;
  }
}
</style>


