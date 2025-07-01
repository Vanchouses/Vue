<template>
    <div class="email-container">
        <div class="container">
            <div class="text">
                <h2 class="section-title">Join the club and get the benefits</h2>
                <p class="section-subtitle">Sign up for our newsletter and receive exclusive 
                offers on new ranges, sales, pop up stores and more</p>
            </div>
            <div class="text-input">
                <input type="text" placeholder="your@email.com" v-model="inputValue">
                <button class="sign-up" @click="addEmail">Sign up</button>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const inputValue = ref('');
const myObject = ref({});

const addEmail = () => {
  if (inputValue.value.trim()) {
    const key = `item_${Date.now()}`;
    myObject.value[key] = inputValue.value;
    inputValue.value = '';
    console.log(myObject.value[key]);
  }
};
</script>

<style scoped>
.email-container {
    background-color: #F9F9F9;
    min-height: 481px;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 40px 20px;
}

.container {
    background-color: white;
    width: 100%;
    max-width: 1200px;
    padding: 40px;
    box-sizing: border-box;
}

.text {
    text-align: center;
    margin-bottom: 40px;
}

.section-title {
    font-family: 'Clash Display', sans-serif;
    font-size: 36px;
    font-weight: 400;
    line-height: 1.2;
    color: #2A254B;
    margin-bottom: 16px;
}

.section-subtitle {
    font-family: 'Satoshi', sans-serif;
    font-size: 16px;
    font-weight: 400;
    color: #505977;
    max-width: 600px;
    margin: 0 auto;
}

.text-input {
    display: flex;
    justify-content: center;
    max-width: 600px;
    margin: 0 auto;
}

input {
    background-color: #F9F9F9;
    padding: 16px 24px;
    width: 100%;
    border: 1px solid #E5E5E5;
    font-family: 'Satoshi', sans-serif;
    font-size: 16px;
    box-sizing: border-box;
}

.sign-up {
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
    white-space: nowrap;
}

.sign-up:hover {
    background: #4a4466;
    box-shadow: 0 4px 12px rgba(42, 37, 75, 0.2);
}

/* Мобильная версия */
@media (max-width: 768px) {
    .email-container {
        padding: 40px 16px;
        min-height: auto;
    }
    
    .container {
        padding: 32px 24px;
    }
    
    .section-title {
        font-size: 28px;
        margin-bottom: 12px;
    }
    
    .section-subtitle {
        font-size: 14px;
    }
    
    .text-input {
        flex-direction: column;
        gap: 12px;
    }
    
    input {
        padding: 14px 20px;
    }
    
    .sign-up {
        width: 100%;
        padding: 14px;
    }
}

@media (max-width: 480px) {
    .section-title {
        font-size: 24px;
    }
    
    .container {
        padding: 24px 16px;
    }
}
</style>