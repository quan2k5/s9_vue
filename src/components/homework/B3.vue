<script setup>
import {ref} from 'vue'
const initialValue=ref('');
</script>
<template>
  <div>
    <input type="date" v-model="initialValue">
    <p>Ngay sinh:{{initialValue}}</p>
  </div>
</template>
<style scoped>
</style>