<template>
  <section class="pets__card" id="pets">
    <h2 class="pets__header">Our Pets</h2>
    <p class="pets__description">
      Step into our charming Pets, where every furry friend has a story to tell.
    </p>

    <div class="pet__list">
      <div v-for="pet in pets" :key="pet.id" class="pet__card">
        <img :src="pet.image" :alt="pet.name" />
        <div class="card__content">
          <h3>{{ pet.name }}</h3>
          <p>Age: {{ pet.Age }}</p>
          <p>Gender: {{ pet.Gender }}</p>
          <button>details</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import dog from '../assets/dog.jpg'
import cat from '../assets/cat.jpg'
import rabbit from '../assets/rabbit.jpg'
import bird from '../assets/bird.jpg'

export default {
  name: 'PetCard',
  data() {
    return {
      pets: [
        { id: 1, name: 'Charlie', type: 'Dog', image: dog, Age: '8 months', Gender: 'Male'},
        { id: 2, name: 'Bella', type: 'Cat', image: cat, Age: '5 months', Gender: 'Famale'},
        { id: 3, name: 'Max', type: 'Rabbit', image: rabbit, Age: '11 months', Gender: 'Male'},
        { id: 4, name: 'Lucy', type: 'Bird', image: bird,  Age: '1 year', Gender: 'Famale'}
      ]
    }
  }
}
</script>

<style>
.pets__card {
  padding: 50px;
  background-color: #f1f7f7;
  color: rgb(66, 66, 66);
}

.pets__header {
  font-size: 2.4rem;
  margin-bottom: 10px;
  text-align: center;
}

.pets__description {
  font-size: 1.1rem;
  margin-bottom: 30px;
  text-align: center;
}

.pet__list {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  justify-self: center;
  gap: 40px;
}

.pet__card {
  background-color: #ffffff;
  border-radius: 15px;
  border: 1px solid rgb(186, 186, 186);
  width: 220px;
  margin: 10px;
  transition: transform 0.3s, box-shadow 0.3s;
}

.pet__card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 10px 10px 0 0;
}

.pet__card .card__content{
  width: 100%;
  padding-inline: 1rem;
  padding-block: .5rem;
}

.pet__card h3 {
  color: rgb(49, 49, 49);
  font-size: 1.6rem;
}

.pet__card p {
  color: rgb(56, 56, 56);
  font-size: 1rem;
  margin-block: 10px;
  font-weight: 600;
}

@media (width < 1190px) {
  .pet__list{
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (width < 576px) {
  .pet__list{
    grid-template-columns: repeat(1, 1fr);
  }
}

</style>
