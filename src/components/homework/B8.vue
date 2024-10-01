<script setup>
import {reactive} from 'vue'
const initialValue= reactive({
    name:'',
    email:'',
   password:'',
    rePassword:'',
});
const handleClick=()=>{
    console.log(initialValue);
}
</script>
<template>
  <div>
    <p>Them moi tai khoan</p>
    <div>
        <label for="">Ho va ten</label>
        <br>
        <input type="text" v-model="initialValue.name">
    </div>
     <div>
        <label for="">Email</label>
        <br>
        <input type="text" v-model="initialValue.email">
    </div>
     <div>
        <label for="">Mat khau</label>
        <br>
        <input type="password" v-model="initialValue.password">
    </div>
     <div>
        <label for="">Nhap lai mat khau</label>
        <br>
        <input type="password" v-model="initialValue.rePassword">
    </div>
    <button  @click="handleClick">Click</button>
  </div>
</template>
<style scoped>
</style>