<script setup>
import {ref} from 'vue'
const initialValue=ref('');

</script>
<template>
  <div>
    <input type="email" v-model="initialValue">
    <p>Gia tri:{{initialValue}}</p>
  </div>
</template>
<style scoped>
</style>
