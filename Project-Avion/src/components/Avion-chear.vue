<template>
    <div class="main-div">
        <section class="hero-banner">
          <div class="text-content">
            <h1 class="headline">The furniture brand for the future, with timeless designs</h1>
            <button class="cta-button">View collection</button>
            <p class="description">
              A new era in eco friendly furniture with Avelon, the French luxury retail brand
              with nice fonts, tasteful colors and a beautiful way to display things digitally
              using modern web technologies.
            </p>
          </div>
          <div class="image-content">
            <img :src="chairImage" alt="Chair"/>
          </div>
        </section>
    </div>
</template>

<script setup>
import chairImage from '../assets/RightImage.svg';
</script>

<style scoped>

.hero-banner {
  display: flex;
  flex-wrap: wrap;
  min-height: 500px;
  background: #ffffff;
  margin-bottom: 80px;
  margin-top: 40px;
}

.text-content {
  flex: 1;
  background-color: #2A254B;
  color: #fff;
  padding: 3rem 2rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.headline {
  font-size: 2rem;
  font-weight: 500;
  margin-bottom: 1.5rem;
  line-height: 1.4;
}

.cta-button {
  background-color: #44425a;
  color: white;
  border: none;
  padding: 0.75rem 1.5rem;
  font-size: 1rem;
  margin-bottom: 2rem;
  cursor: pointer;
  width: 10rem;
  height: 4rem;
}

.cta-button:hover {
  background-color: #5a5770;
}

.description {
  font-size: 0.95rem;
  color: #ddd;
  max-width: 80%;
}

.image-content {
  flex: 1;
  background-color: #83a5a7;
  display: flex;
  justify-content: center;
  align-items: center;
}

.image-content img {
  max-width: 100%;
  height: auto;
  object-fit: contain;
}
</style>
