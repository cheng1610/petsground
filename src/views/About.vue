<template>
  <section class="about" id="about">
    <div class="about__container">
      <div class="about__text">
        <h2>About Our Pet Paradise</h2>
        <p>
          Founded with love and passion, our Pet Paradise brings together the finest pets and high-quality treats in English style. We are committed to providing a safe, caring environment where every pet can thrive.
        </p>
        <button>Learn More</button>
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
:root {
  --bg-card: #38736D;
  --accent-hover: #246534;
  --text-main: #ffffff;
}

.about {
  background-color: #465b52;
  color: var(--text-main);
  padding: 80px 50px;
}

.about__container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 40px;
  max-width: 1200px;
  margin: 0 auto;
}

.about__text {
  flex: 1;
  min-width: 300px;
}

.about__text h2 {
  font-size: 2.2rem;
  margin-bottom: 20px;
  color: #183b3b;
}

.about__text p {
  font-size: 1.1rem;
  line-height: 1.7;
  color: #d9e9de;
  margin-bottom: 15px;
}


@media (max-width: 1024px) {
  .about__container {
    flex-direction: column;
    text-align: center;
  }

  .about__text {
    margin-top: 20px;
  }
}

@media (max-width: 600px) {
  .about {
    padding: 50px 25px;
  }

  .about__text h2 {
    font-size: 1.8rem;
  }

  .about__text p {
    font-size: 1rem;
  }
}
</style>
