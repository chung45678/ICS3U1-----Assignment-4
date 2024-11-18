<script setup>
import { ref } from 'vue';

const iterations = ref(0);
const approximatePi = ref(0);

function findLeibniz() {
    let a = 0;
    for (let i = 0; i < iterations.value; i++) {
        a += (i % 2 === 0 ? 1 : -1) / (2 * i + 1);
    }
    approximatePi.value = a * 4;
}
</script>

<template>
  <form @submit.prevent="findLeibniz">

    <label>Iterations (n): </label>
    <input v-model="iterations" type="number" />
    <label>Pi Approximation (Result): </label>
    <input v-model="approximatePi" type="number" readonly />
    <input type="submit" value="Approximate Pi" />
  </form>
</template>

<style scoped>
body {
    font-family: Arial, sans-serif;
    margin: 20px;
    text-align: center;
    justify-content: center;
    align-items: center;
    background-color: darkgray;

}

section {
    text-align:center;
    justify-content: center;
    align-items: center;
    margin-bottom: 20px;
    padding: 10px;
    background-color: rgb(255, 255, 255);
    padding: 20px;
    max-width: 400px;
    
    
}

label {
    text-align: center;
    display: block;
    margin: 10px 0px;
}

button {
    background-color: rgb(10, 126, 204);
    color: white;
    border: none;
    padding: 8px 16px;
    border-radius: 4px;

}

.row {
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
    
}

label {
    display: block;
    margin: 10px 0px 5px;
    font-weight: 600;
    color: black;
    text-align: left;
}

.container {
    display:flex;
    gap: 30px;
    width: 800px;
    flex-wrap: wrap;
}
</style>
