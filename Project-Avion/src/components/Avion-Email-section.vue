<template>
    <div class="email-container">
        <div class="container">
            <div class="text">
                <h2 class = "section-title">Join the club and get the benefits</h2>
                <p>Sign up for our newsletter and receive exclusive 
                offers on new ranges, sales, pop up stores and more</p>
            </div>
            <div class="text-input">
                <input type="text" placeholder="your@email.com" v-model="inputValue">
                <button class="sign-up" @click = "addEmail">Sign up</button>
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

<style>
.email-container{
    background-color: #F9F9F9;
    height: 481px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.container {
    background-color: white;
    width: 80%;
    height: 70%;
}
.text {
    display: block;
    text-align: center;
}
.section-title{
    font-family: 'Clash Display', sans-serif;
    font-size: 36px;
    font-weight: 400;
    line-height: 1.4;
    color: #2A254B;
    margin-bottom: 10px;
    margin-top: 80px;
    text-align: left;
    display: inline-block;
}
p {
    font-family: 'Clash Display', sans-serif;
    font-size: 16px;
    font-weight: 400;
}
.text-input {
    display: flex;
    justify-self: center;
    margin-top: 60px;
}

input {
    background-color: #F9F9F9;
    padding: 16px;
    width: 354px;
    border-right: none;
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
}

.sign-up:hover {
  background: #4a4466;
  box-shadow: 0 4px 12px rgba(42, 37, 75, 0.2);
}
</style>