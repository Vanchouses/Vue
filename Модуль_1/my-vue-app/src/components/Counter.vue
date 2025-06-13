<template>
    <h4 class="homework">Задание 2</h4>
    <h1>Счетчик: {{ count }}</h1>
    <button @click = "decrement">Убавить ➖</button>
    <button @click ="increment">Прибавить ➕</button>
    <hr>
</template>

<script setup>
import {ref} from 'vue'

const count = ref(0); 

function decrement() {
    return count.value--;
}

function increment() {
    return count.value++;
}
</script>

<style scoped>
h1 {
    color:blueviolet;
}
button {
    color: blueviolet;
    background-color: aqua;
    margin: 10px;
    width: 150px;
    padding: 10px;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    font-weight: bold;
}

.homework {
    color:aquamarine;
}
</style>