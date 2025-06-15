<template>
  <header class="header">
    <div class="left-icons">
      <i class="fas fa-search icon"></i>
    </div>
    <div class="logo">Avion</div>
    <div class="right-icons">
      <i class="fas fa-shopping-cart icon"></i>
      <i class="far fa-user icon"></i>
    </div>
  </header>
</template>

<script setup>
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  border-bottom: 1px solid #ddd;
  font-family: 'Inter', sans-serif;
}

.left-icons,
.right-icons {
  display: flex;
  gap: 1.5rem;
}

.logo {
  font-size: 1.25rem;
  font-weight: 500;
  color: #2D2C2C;
}

.icon {
  font-size: 1.2rem;
  color: #3C3C3C;
  cursor: pointer;
}
</style>