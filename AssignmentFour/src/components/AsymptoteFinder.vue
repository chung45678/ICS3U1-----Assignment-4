<script setup>
import { ref } from 'vue';

const numerator = ref(0);
const denominator = ref(0);
const asymptote = ref('');

function asymptoteFinder() {
    if (numerator.value === denominator.value) {
        asymptote.value = "The asymptote is horizontal";
    } else if (denominator.value > numerator.value) {
        asymptote.value = "The asymptote is the x-axis";
    } else {
        const degreeDifference = numerator.value - denominator.value;
        const names = ["Linear", "Quadratic", "Cubic", "Quartic", "Quintic", "Sextic", "Septic", "Octic", "Nonic", "Decic"];
        asymptote.value = names[degreeDifference - 1] || "Higher-degree asymptote";
    }
}
</script>

<template>
  
  <form @submit.prevent="asymptoteFinder">
    <h2> Asymptote Finder</h2>
    <label>Degree of Numerator (m): </label>
    <input v-model="numerator" type="number" />
    <label>Degree of Denominator (n): </label>
    <input v-model="denominator" type="number" />
    <label>Asymptote Type (Result): </label>
    <input v-model="asymptote" type="text" readonly />
    <input type="submit" value="Find Asymptote" />
  </form>
</template>

<style scoped>

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

h2 {
  margin-top: 0;
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
input {
  background-color: white;
  color:black;
  border-radius:4px;
}

input[type="submit"] {
    background-color: rgb(105, 179, 240);
    border-color: black;
    margin: 4px;
}
.container {
    display:flex;
    gap: 30px;
    width: 800px;
    flex-wrap: wrap;
}
</style>
