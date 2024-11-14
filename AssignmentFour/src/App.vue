<script setup>
import CosineLaw from './components/CosineLaw.vue';
</script>

<template>
  <div class="app-container">
    <CosineLaw />

  </div>
</template>

<style scoped>
.app-container {
    display: grid;
    grid-template-columns: 45vw 45vw;
    gap: 100px;
}
</style>