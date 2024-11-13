<script setup>
import { ref } from 'vue';

const aValue = ref(0);
const bValue = ref(0);
const cValue = ref(0);

function pythagoreanTheorem() {
  cValue.value = Math.sqrt(aValue.value * aValue.value + bValue.value * bValue.value);
}
</script>

<template>
  <form @submit.prevent="pythagoreanTheorem()">
    <label>a Value:</label>
    <input v-model="aValue" type="number" />
    <label>b Value:</label>
    <input v-model="bValue" type="number" />
    <label>c Value (Result):</label>
    <input v-model="cValue" type="number" readonly />
    <input type="submit" value="Calculate" />
  </form>
</template>

<style scoped>

</style>