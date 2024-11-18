<script setup>
import { ref } from 'vue';

const aSide = ref(0);
const bSide = ref(0);
const cAngle = ref(0);
const cSide = ref(0);

function cosineLaw() {
    cSide.value = Math.sqrt(
        aSide.value ** 2 +
        bSide.value ** 2 -
        2 * aSide.value * bSide.value * Math.cos(cAngle.value * (Math.PI / 180))
    );
}
</script>

<template>
  <form @submit.prevent="cosineLaw">
    <h2>Cosine Law</h2>
    <label>a Side Value: </label>
    <input v-model="aSide" type="number" />
   
    <label>b Side Value: </label>
    <input v-model="bSide" type="number" />  
    <label>c Angle Value: </label>
    <input v-model="cAngle" type="number" /> 
    <label>c Side (Result): </label>
    <input v-model="cSide" type="number" readonly />
    <input type="submit" value="Calculate" />
    
    
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

label {
    text-align: center;
    display: block;
    margin: 10px 0px;
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
h2 {
  margin-top: 0;
}

.container {
    display:flex;
    gap: 30px;
    width: 800px;
    flex-wrap: wrap;
}
</style>
