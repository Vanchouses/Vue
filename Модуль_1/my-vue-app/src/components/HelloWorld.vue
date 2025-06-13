<template>
    <div>
        <h4 class="homework">Задание 1</h4>
        <h1>{{ message }}</h1>
        <button @click = "changeMassage">Сменить сообщение</button>
        <hr>
    </div>
</template>

<script setup>
import {ref} from 'vue'

const message = ref('Привет Vue 3 с Compasition API')

function changeMassage() {
    message.value = prompt("NewMessage");
}
</script>

<style scoped>
h1 {
    color: aqua;
}

button{
    background-color:aqua;
    color:blueviolet;
}

.homework {
    color:aquamarine;
}
</style>