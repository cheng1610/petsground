<template>
  <section class="about" id="about">
    <div class="about__container">
      <div class="about__text">
        <h2>About PetsGround</h2>
        <p>
          At PetsGround, we believe every pet deserves a loving home and a happy life. 
          We provide a safe and joyful environment where pets and pet lovers can come together.
        </p>
        <p>
          From adoption support to interactive zones and pet-friendly cafes, our mission is to bring happiness 
          to pets and their humans alike. Join us and discover a community built with care and passion.
        </p>
      </div>
      <div class="about__image">
        <img src="../assets/about.jpg" alt="Happy Pets" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "About",
};
</script>

<style>
.about {
  padding: 60px 5rem;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #424242;
}

.about__container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  max-width: 1200px;
  width: 100%;
}

.about__text {
  flex: 1;
  min-width: 300px;
  margin-right: 2rem;
}

.about__text h2 {
  font-size: 2.5rem;
  margin-bottom: 20px;
}

.about__text p {
  font-size: 1.2rem;
  line-height: 1.7;
  margin-bottom: 15px;
}

.about__image {
  flex: 1;
  min-width: 300px;
  text-align: center;
}

.about__image img {
  width: 100%;
  max-width: 450px;
  border-radius: 15px;
  border: 6px rgb(149, 132, 132) solid;
  object-fit: cover;
  transition: all .3s ease;
}

.about__image img:hover{
  transform: rotate(10deg);
}

@media (width < 1024px) {
  .about__container {
    flex-direction: column;
    text-align: center;
  }

  .about__text {
    margin-right: 0;
    margin-bottom: 30px;
  }

  .about__text h2 {
    font-size: 2rem;
  }

  .about__text p {
    font-size: 1rem;
  }
}
</style>