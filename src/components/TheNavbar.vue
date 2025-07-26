<template>
  <nav class="navbar is-fixed-top" role="navigation" aria-label="main navigation">
    <div class="container">
      <div class="navbar-brand">
        <a class="navbar-item is-size-4 has-text-weight-semibold" href="#home">
          Dayanne & Jhon❤️
        </a>
        <a role="button" class="navbar-burger" :class="{ 'is-active': isActive }" @click="toggleMenu" aria-label="menu" aria-expanded="false" data-target="navbarMenu">
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>
      <div id="navbarMenu" class="navbar-menu" :class="{ 'is-active': isActive }">
        <div class="navbar-end">
          <a class="navbar-item " href="#home">
            Início
          </a>
          <a class="navbar-item" href="#historia" @click="closeMenu">
            Nossa História
          </a>
          <a class="navbar-item" href="#padrinhos" @click="closeMenu">
            Padrinhos
          </a>
          <a class="navbar-item" href="#presentes" @click="closeMenu">
            Lista de Presentes
          </a>
        </div>
      </div>
    </div>
  </nav>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
export default defineComponent({
  name: 'TheNavbar',
  setup() {
    const isActive = ref(false);
    const toggleMenu = () => { isActive.value = !isActive.value; };
    const closeMenu = () => { isActive.value = false; };
    return { isActive, toggleMenu, closeMenu };
  },
});
</script>

<style scoped>
.navbar {
  background-color: rgba(20, 20, 20, 0.4);
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
}
.navbar-item, .navbar-burger {
  color: white;
  font-weight: 500;
}
.navbar-item:hover, .navbar-brand > .navbar-item:hover {
  background-color: rgba(255, 255, 255, 0.1) !important;
  color: white !important;
}
.navbar-burger span {
  background-color: white;
}
</style>