<template>
    <h4 class="homework">Задание 3</h4>
    <h1>Счетчик: {{ count }}</h1>
    <button @click = "decrement">Убавить ➖</button>
    <button @click ="increment">Прибавить ➕</button>
    <h2>{{ parity }}</h2>
    <hr>
</template>

<script setup>
import {ref, computed} from 'vue'

const count = ref(0); 

function decrement() {
    return count.value--;
}

function increment() {
    return count.value++;
}

const parity = ref(computed(() => count.value % 2 === 0 ? "Чётное" : "Нечётное"));
</script>

<style scoped>
h1 {
    color:blueviolet;
}
h2 {
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