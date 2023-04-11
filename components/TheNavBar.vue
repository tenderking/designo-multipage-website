
<script setup lang="ts">
 //use vue-use to toggle menu-toggle
import { useToggle } from '@vueuse/core'

const [isMenuOpen, toggleMenu] = useToggle()

</script>
<template>
  <nav>
      <NuxLink to="/">
          <img src="/assets/shared/desktop/logo-dark.png" class="logo-dark" />
      </NuxLink>
      <div class="menu-toggle" @click="toggleMenu">
        <span></span>
        <span></span>
        <span></span>
      </div>
      <ul class="menu" :class="{ 'active': isMenuOpen }">
        <li>
          <NuxLink to="/">Our Company</NuxLink>
        </li>
        <li>
          <NuxLink to="/about">Locations</NuxLink>
        </li>
        <li>
          <NuxLink to="/contact">Contact</NuxLink>
        </li>
      </ul>
  </nav>
</template>

<style scoped>
nav{
 display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo-dark{
width:202px;
}
.menu-toggle {
  display: none;
  cursor: pointer;
}

.menu-toggle span {
  display: block;
  height: 2px;
  width: 25px;
  margin-bottom: 5px;
  background-color: #333;
}

.menu {
  display: flex;
  justify-content: center;
  align-items: center;
  list-style: none;
  margin: 0;
  padding: 0;
}

.menu li {
  margin-left: 20px;
}
@media screen and (max-width: 768px) {
  .menu {
    display: none;
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    text-align: center;
    padding: 20px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
  }

  .menu.active {
    display: flex;
    flex-direction: column;
  }

  .menu li {
    margin: 10px 0;
  }

  .menu-toggle {
    display: block;
  }
}
</style>


