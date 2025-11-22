<template>
  <section class="home" id="home">
    <div class="content">
      <h2>Welcome to PetsGround</h2>
      <p>  Discover a paradise for pets and pet lovers alike. From playful companions to high-quality treats</p>
      <div class="buttons">
        <button>Explore Now</button>
        <button class="start__it">Start it</button>
      </div>
    </div>
    <div class="banner">
      <img src="../assets/banner.jpg" alt="Pet Food" />
    </div>
  </section>
</template>

<script>
export default {
  name: "Home",
};
</script>

<style>
.home {
  display: flex;
  justify-content: space-around;
  align-items: center;
  background-size: cover;
  background-position: center;
  padding-inline: 7rem;
  padding-block: 1rem;
  color: white;
  flex-wrap: wrap; 
}

.content {
  max-width: 50%;
  color: black;
}

.content h2 {
  font-size: 3rem;
  margin-bottom: 15px;
}

.content p {
  font-size: 1.5rem;
  margin-bottom: 20px;
}

.buttons {
  display: flex;
  flex-wrap: wrap;
}

button {
  background-color: #38736D;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 8px;
  font-size: 1rem;
  cursor: pointer;
  transition: all 0.3s ease;
}

.start__it {
  background-color: transparent;
  border: #38736D 2px solid;
  color: rgb(66, 66, 66);
  margin-left: 15px;
  transition: all 0.3s ease;
}

.start__it:hover {
  background-color: #38736D;
  color: white;
}

.banner img {
  width: 400px;
  height: auto;
  object-fit: cover;
}

@media (width < 1024px) {
  .home {
    flex-direction: column;
    text-align: center;
    padding-inline: 3rem;
  }

  .content {
    max-width: 90%;
  }

  .content h2 {
    font-size: 2.2rem;
  }

  .content p {
    font-size: 1.2rem;
  }

  .buttons{
    justify-content: center;
  }

  .banner img {
    width: 300px;
    margin-top: 20px;
  }
}

@media (width < 600px) {
  .home {
    padding-inline: 1.5rem;
    padding-block: 2rem;
  }

  .content h2 {
    font-size: 1.8rem;
  }

  .content p {
    font-size: 1rem;
  }

  .buttons {
    gap: 10px;
  }

  .start__it {
    margin-left: 0;
  }

  .banner img {
    width: 100%;
    max-width: 280px;
  }
}
</style>
