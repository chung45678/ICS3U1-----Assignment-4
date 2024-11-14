<script setup>
import { ref } from 'vue';

const aSide = ref(0);
const bSide = ref(0);
const cAngle = ref(0);
const cSide = ref(0);

function cosineLaw() {
    cSide.value = Math.sqrt(aSide ** 2 + bSide ** 2 - 2 * aSide * bSide * Math.cos(cAngle * (Math.PI / 180)));

}
</script>

<template>
  <form @submit.prevent="cosineLaw()">
    <label>a Side Value:</label>
    <input v-model="aSide" type="number" />
    <label>b Side Value:</label>
    <input v-model="bSide" type="number" />
    <label>c Angle Value:</label>
    <input v-model="cAngle" type="number" />
    <label>c side (Result):</label>
    <input v-model="cSide" type="number" readonly />
    <input type="submit" value="Calculate" />
  </form>
</template>

<style scoped>

</style>