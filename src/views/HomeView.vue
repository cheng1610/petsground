<template>
  <div >
    <Header />
    <Home />
    <Service></Service>
    <PetCard />
    <Footer />
  </div>
</template>

<script>
import Header from '../components/Header.vue'
import Home from '../components/Home.vue'
import Service from '../components/Service.vue'
import PetCard from '../components/PetCard.vue'
import Footer from '../components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Home,
    Service,
    PetCard,
    Footer
  }
}

</script>

<style>

</style>
