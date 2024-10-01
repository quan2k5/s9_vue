<script setup>
import {ref} from 'vue'
const initialValue=ref('Nam');
</script>
<template>
  <div>
    <p>Gioi tinh:{{initialValue}}</p>
    <div>
        <input  id='nam' type="radio" value="Nam" v-model="initialValue">
        <label  id for="nam">Nam</label>
    </div>
      <div>
        <input  id='nư' type="radio" value="Nữ" v-model="initialValue">
        <label  id for="nư">Nữ</label>
    </div>
      <div>
        <input  id='other' type="radio" value="khac" v-model="initialValue">
        <label  id for="other">Khac</label>
    </div>
  </div>
</template>
<style scoped>
</style>