<template>
  <header class="header">
    <h3>Petsground</h3>
    <nav>
      <a href="#home">Home</a>
      <a href="#service">Service</a>
      <a href="#pets">Pets</a>
      <RouterLink to="/about">About</RouterLink>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style>
.header {
  background-color: #35605d;
  font-size: 1.2rem;
  color: white;
  padding: 1rem 5rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.header nav a {
  color: white;
  margin-left: 20px;
  text-decoration: none;
  font-weight: bold;
}

</style>
