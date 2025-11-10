<template>
  <section class="services__section" id="service">
    <h2 class="services__header">Our Services</h2>
    <p class="service__description description">Explore our Pets Gallery to find your new best friend — full of love, joy, and wagging tails.</p>
    <div class="services__container">
      <div v-for="(service, index) in services" :key="index" class="service__card">
        <component :is="service.icon" class="card__icon" />
        <h3 class="card__title">{{ service.title }}</h3>
        <p class="card__description">{{ service.description }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
import { PawPrint, Coffee, GraduationCap } from "lucide-vue-next";

const services = [
  {
    icon: PawPrint,
    title: "Pet Interaction Zone",
    description: "Get up close and personal with adorable animals, feed them and play with them."
  },
  {
    icon: Coffee,
    title: "Pet Café",
    description: "Enjoy aromatic coffee and desserts, and relax in the company of your furry friend."
  },
  {
    icon: GraduationCap,
    title: "Adoption & Care Workshop",
    description: "Learn about adoption and care so that love can extend to every animal."
  }
];
</script>

<style scoped>
.services__section {
  background-color: #fafafa;
  padding: 80px 20px;
  text-align: center;
  color: rgb(66, 66, 66);
}

.services__header {
  font-size: 2.4rem;
  margin-bottom: 10px;
}

.service__description{
    font-size: 1.1rem;
    margin-bottom: 30px;
}

.services__container {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 30px;
}

.service__card {
  background-color: #fff;
  width: 280px;
  border-radius: 16px;
  padding: 30px 20px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
}

.service__card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 18px rgba(0, 0, 0, 0.15);
}

.card__icon {
  width: 48px;
  height: 48px;
  color: #4b7a76;
  margin-bottom: 15px;
}

.card__title {
  font-size: 1.3rem;
  font-weight: 600;
  color: #444;
  margin-bottom: 10px;
}

.card__description {
  color: #666;
  font-size: 0.95rem;
  line-height: 1.6;
}
</style>
