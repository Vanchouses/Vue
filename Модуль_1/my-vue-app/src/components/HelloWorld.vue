<template>
    <div>
        <h1>{{ message }}</h1>
        <button @click = "changeMassage">Сменить сообщение</button>
    </div>
</template>

<script setup>
import {ref} from 'vue'

const message = ref('Привет Vue 3 с Compasition API')

function changeMassage() {
    message.value = "NewMassage";
}
</script>

<style scoped>
h1 {
    color: aqua;
}
</style>