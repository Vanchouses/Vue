<template>
  <section class="products-section">
    <h2 class="section-title">New ceramics</h2>
    
    <div class="products-grid">
      <div 
        v-for="product in products" 
        :key="product.id" 
        class="product-card"
      >
        <img 
          :src="product.image" 
          :alt="product.alt" 
          class="product-image"
        >
        <h3 class="product-title">{{ product.title }}</h3>
        <p class="product-price">{{ product.price }}</p>
      </div>
    </div>
    
    <button class="view-collection-btn">View collection</button>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import ProductCard1 from '../assets/ProductCard.png'
import ProductCard2 from '../assets/ProductCard1.png'
import ProductCard3 from '../assets/ProductCard2.png'
import ProductCard4 from '../assets/ProductCard3.png'

const products = ref([
  {
    id: 1,
    title: 'The Dandy chair',
    price: '£250',
    image: ProductCard1,
    alt: 'The Dandy chair'
  },
  {
    id: 2,
    title: 'Rustic Vase Set',
    price: '£155',
    image: ProductCard2,
    alt: 'Rustic Vase Set'
  },
  {
    id: 3,
    title: 'The Silky Vase',
    price: '£125',
    image: ProductCard3,
    alt: 'The Silky Vase'
  },
  {
    id: 4,
    title: 'The Lucy Lamp',
    price: '£399',
    image: ProductCard4,
    alt: 'The Lucy Lamp'
  }
])
</script>

<style scoped>
/* Основные стили секции */
.products-section {
  max-width: 1200px;
  margin: 0 auto;
  padding: 60px 20px;
  position: relative;
}

/* Заголовок секции */
.section-title {
  font-family: 'Clash Display', sans-serif;
  font-size: 32px;
  font-weight: 400;
  line-height: 1.4;
  color: #2A254B;
  margin-bottom: 40px;
  text-align: left;
  position: relative;
  display: inline-block;
}

.section-title::after {
  content: '';
  position: absolute;
  bottom: -10px;
  left: 0;
  width: 80px;
  height: 1px;
  background: #2A254B;
}

/* Сетка товаров */
.products-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 40px 20px;
  margin-bottom: 50px;
}

/* Карточка товара */
.product-card {
  text-align: left;
  transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
  position: relative;
  overflow: hidden;
}

.product-card:hover {
  transform: translateY(-5px);
}

/* Изображение товара */
.product-image {
  width: 100%;
  height: 380px;
  object-fit: cover;
  margin-bottom: 20px;
  transition: transform 0.5s ease;
  background: #f9f9f9;
}

.product-card:hover .product-image {
  transform: scale(1.03);
}

/* Название товара */
.product-title {
  font-family: 'Clash Display', sans-serif;
  font-size: 20px;
  font-weight: 400;
  color: #2A254B;
  margin-bottom: 12px;
  letter-spacing: 0.5px;
}

/* Цена товара */
.product-price {
  font-family: 'Satoshi', sans-serif;
  font-size: 18px;
  font-weight: 400;
  color: #2A254B;
  display: block;
}

/* Кнопка View Collection */
.view-collection-btn {
  font-family: 'Satoshi', sans-serif;
  font-size: 16px;
  font-weight: 400;
  background: #2A254B;
  color: white;
  border: none;
  padding: 16px 32px;
  cursor: pointer;
  transition: all 0.3s ease;
  letter-spacing: 0.5px;
  text-transform: uppercase;
  display: inline-block;
  margin-top: 20px;
}

.view-collection-btn:hover {
  background: #4a4466;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(42, 37, 75, 0.2);
}

/* Адаптивность */
@media (max-width: 1024px) {
  .products-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (max-width: 768px) {
  .products-section {
    padding: 40px 20px;
  }
  
  .products-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 30px 15px;
  }
  
  .product-image {
    height: 300px;
  }
  
  .section-title {
    font-size: 28px;
    margin-bottom: 30px;
  }
}

@media (max-width: 480px) {
  .products-grid {
    grid-template-columns: 1fr;
  }
  
  .product-image {
    height: 250px;
  }
  
  .section-title {
    font-size: 24px;
  }
  
  .view-collection-btn {
    width: 100%;
    text-align: center;
  }
}

/* Дополнительные эффекты */
.product-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(to bottom, rgba(0,0,0,0) 0%, rgba(0,0,0,0.03) 100%);
  pointer-events: none;
  z-index: 1;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.product-card:hover::before {
  opacity: 1;
}
</style>
