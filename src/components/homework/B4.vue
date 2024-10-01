<script setup>
import {ref} from 'vue'
const initialValue=ref(0);
</script>
<template>
  <div>
    <p>Tien do hoan thanh {{initialValue}}%</p>
    <input type="range" v-model="initialValue">
  </div>
</template>
<style scoped>
</style>