<template>
  <nav class="category-nav">
    <ul>
      <li v-for="category in categories" :key="category" class="nav-item">
        <a href="#" class="nav-link">{{ category }}</a>
      </li>
    </ul>
  </nav>
</template>

<script setup>
const categories = [
  'Plant pots',
  'Ceramics',
  'Tables',
  'Chairs',
  'Crockery',
  'Tableware',
  'Cutlery'
];
</script>

<style scoped>
.category-nav {
  border-top: 1px solid #e0e0e0;
  padding: 1rem 2rem;
  text-align: center;
}

ul {
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 2rem;
  padding: 0;
  margin: 0;
}

.nav-link {
  color: #6f6f7b;
  text-decoration: none;
  font-size: 0.95rem;
  transition: color 0.2s ease;
}

.nav-link:hover {
  color: #2d2c2c;
}
</style>
