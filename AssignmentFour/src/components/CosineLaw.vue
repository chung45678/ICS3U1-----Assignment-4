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
