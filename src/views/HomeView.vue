<template>
  <main class="main">
    <h1 :style="{ color: textColor }">{{ pageTitle }}</h1>
    <p :class="{ 'highlight': isHighlighted }">Ketik Sembarang Ajalah</p>
    <input type="text" v-model="inputText" @input="updateText">
    <p>{{ inputText }}</p>
  </main>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const pageTitle = 'Pemrograman Berbasis Komponen';
const isHighlighted = ref(false);
const inputText = ref('');
const textColor = ref('white');

const updateText = (event: Event) => {
  inputText.value = (event.target as HTMLInputElement).value;
  textColor.value = inputText.value.length >= 1 ? 'cyan' : 'white';
};
</script>

<style>
body {
  color: white;
  background-image: url('/src/assets/Bulan.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.main {
  text-align: center;
}

h1 {
  font-size: 48px;
  margin-bottom: 20px;
}

p {
  font-size: 24px; 
  line-height: 1.5;
}

input {
  padding: 10px;
  font-size: 16px;
  border: 2px solid white;
  border-radius: 5px;
  margin-bottom: 20px;
}

.highlight {
  background-color: white; 
}
</style>
