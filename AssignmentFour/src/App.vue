<script setup>
import CosineLaw from './components/CosineLaw.vue';
import AsymptoteFinder from './components/AsymptoteFinder.vue';
import GregoryLeibnizPi from './components/GregoryLeibniz.vue';
</script>

<template>
  <div class="app-container">
    <h1>Assignment 4 - Vite & Vue</h1>
    <CosineLaw />
    <AsymptoteFinder />
    <GregoryLeibnizPi />
  </div>
</template>

<style scoped>
form {
  text-align: start;
  margin-bottom: 20px;
  padding: 10px;
  background-color: rgb(255, 255, 255);
  padding: 40px;
  max-width: 400px;
  border-radius: 16px;
}

.app-container {
  display:flex;
  gap: 30px;
  width: 900px;
  flex-wrap: wrap;
  color: black;

}

h1 {
  color:white;
}

label {
  display: inline;
  color: black;
  margin: 40px;
}

input {
  color:rgb(109, 148, 255);
  background-color: white;
}

</style>
