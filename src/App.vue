<script setup>
import { ref } from 'vue';

const count = ref(0);

const increase = () => count.value++;
const decrease = () => count.value--;
const reset = () => { count.value = 0; }
</script> 

<template>
  <main class="container">
    <h1>Muertes Zooldyck: {{ count }}</h1>
    <div class="buttons-container">
      <button @click="increase" class="button death"> Se murió ☠️</button>
      <button @click="decrease" class="button life">Vida extra ❤️‍🩹</button>
    </div>
    <button @click="reset" class="button reset">Reiniciar 🔄️</button>

  </main>
</template>

<style scoped>
.container {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.buttons-container {
  display: flex;
  gap: 10px;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
}

.button {
  margin-top: 8px;
  width: 200px;
  height: 30px;
  border-radius: 8px;
  border: none;
  font-weight: 600;
}

.death {
  background-color: #fa5b5b;
}

.reset {
  background-color: #4a77ca;
}

.life {
  background-color: #298854;
}
</style>
