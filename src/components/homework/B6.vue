<script setup>
import {ref} from 'vue'
const sports=['da bong','bong chuyen','code','boi loi']
const initialValue=ref([]);
</script>
<template>
  <div>
    <ul>
        <li>So thich: {{initialValue}}</li>
        <li :key="item" v-for="item in sports">   
            <input :id="item" type="checkbox" :value="item" v-model="initialValue">
            <label for="" :id="item">{{item}}</label>
        </li>
    </ul>
  </div>
</template>
<style scoped>
</style>