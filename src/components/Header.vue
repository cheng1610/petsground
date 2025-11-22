<template>
  <header class="header">
    <h3 class="logo">Petsground</h3>
    <TextAlignJustify class="menu__btn" @click="toggleMenu"/>
    <nav :class="{ open: isOpen }" @click="closeMenu">
      <RouterLink to="/" @click="closeMenu">Home</RouterLink>
      <a href="#service" @click="closeMenu">Service</a>
      <a href="#pets" @click="closeMenu">Pets</a>
      <RouterLink to="/about" @click="closeMenu">About</RouterLink>
    </nav>
  </header>
</template>

<script setup>
import { ref } from 'vue'
import { TextAlignJustify } from 'lucide-vue-next'

const isOpen = ref(false)
const toggleMenu = () => (isOpen.value = !isOpen.value)
const closeMenu = () => (isOpen.value = false)
</script>

<style>
.header {
  background-color: #35605d;
  font-size: 1.2rem;
  color: white;
  padding: 1rem 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-weight: bold;
}

nav {
  display: flex;
  gap: 20px;
}

.menu__btn {
  display: none;
  cursor: pointer;
}


@media (width < 768px) {
  nav {
    position: fixed;
    top: 0;
    right: -250px;
    width: 200px;
    height: 100vh;
    background: #35605d;
    display: flex;
    flex-direction: column;
    padding-top: 80px;
    padding-left: 20px;
    gap: 20px;
    transition: right 0.3s ease;
  }

  nav.open {
    right: 0;
  }

  .menu__btn {
    display: block;
  }
}
</style>
