<template>
  <div class="profile">
    <h4 class="homework">Задание 4</h4>

    <h2>Профиль пользователя</h2>

    <label>
      Имя:
      <input v-model="user.name" type="text" placeholder="Введите имя" />
    </label>

    <label>
      Возраст:
      <input v-model.number="user.age" type="number" placeholder="Введите возраст" />
    </label>

    <p class="greeting">{{ greeting }}</p>
  </div>
</template>

<script setup>
import { reactive, computed, watch } from 'vue'

const user = reactive({
  name: '',
  age: 0
})

const greeting = computed(() => {
  return `Привет, ${user.name || 'гость'}! Тебе ${user.age || '...'} лет.`
})

watch(() => user.age, (newAge) => {
  console.log('Возраст изменился:', newAge)
})
</script>

<style scoped>
.profile {
  max-width: 400px;
  margin: 0 auto;
  padding: 20px;
  font-family: sans-serif;
  color:blueviolet;
}

label {
  display: block;
  margin-bottom: 12px;
  font-weight: bold;
  color:aqua;
}

input {
  display: block;
  width: 100%;
  padding: 8px;
  margin-top: 4px;
  border-radius: 6px;
  border: 3px solid #b250bd;
}

.greeting {
  margin-top: 20px;
  font-size: 18px;
  color: blueviolet;
}

.homework {
    color:aquamarine;
}
</style>