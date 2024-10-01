<script setup>
import {ref} from 'vue'
const initialValue=ref('#ff0000');
</script>
<template>
  <div>
    <input type="color" v-model="initialValue">
    <p>Gia tri:{{initialValue}}</p>
  </div>
</template>
<style scoped>
</style>