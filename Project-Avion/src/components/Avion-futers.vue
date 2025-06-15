<template>
    <div class="main-div">  
        <section class="features">
          <h2 class="features__title">What makes our brand different</h2>
          <div class="features__grid">
            <div class="feature" v-for="(item, index) in features" :key="index">
              <i :class="item.icon" class="feature__icon"></i>
              <h3 class="feature__heading">{{ item.title }}</h3>
              <p class="feature__description">{{ item.text }}</p>
            </div>
          </div>
        </section>
    </div>
</template>

<script setup>
const features = [
  {
    icon: 'fas fa-truck',
    title: 'Next day as standard',
    text: 'Order before 3pm and get your order the next day as standard'
  },
  {
    icon: 'fas fa-check-circle',
    title: 'Made by true artisans',
    text: 'Handmade crafted goods made with real passion and craftsmanship'
  },
  {
    icon: 'fas fa-credit-card',
    title: 'Unbeatable prices',
    text: 'For our materials and quality you won’t find better prices anywhere'
  },
  {
    icon: 'fas fa-leaf',
    title: 'Recycled packaging',
    text: 'We use 100% recycled packaging to ensure our footprint is manageable'
  }
]
</script>

<style scoped>
.features {
  padding: 3rem 1rem;
  text-align: center;
}

.features__title {
  font-size: 1.5rem;
  margin-bottom: 2rem;
  color: #2e2e4f;
}

.features__grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 2rem;
}

.feature {
  max-width: 220px;
}

.feature__icon {
  font-size: 1.5rem;
  margin-bottom: 0.8rem;
  color: #2e2e4f;
}

.feature__heading {
  font-weight: 600;
  margin-bottom: 0.5rem;
}

.feature__description {
  font-size: 0.9rem;
  color: #555;
}
</style>
