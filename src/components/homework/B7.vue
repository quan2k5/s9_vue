<script setup>
import {reactive} from 'vue'
const initialValue= reactive({
    id:'',
    name:'',
    price:'',
    quantity:0,
});
const handleClick=()=>{
    console.log(initialValue);
}
</script>
<template>
  <div>
    <p>Them moi san pham</p>
    <div>
        <label for="">Ma san pham</label>
        <br>
        <input type="text" v-model="initialValue.id">
    </div>
     <div>
        <label for="">Ten san pham</label>
        <br>
        <input type="text" v-model="initialValue.name">
    </div>
     <div>
        <label for="">Gia</label>
        <br>
        <input type="text" v-model="initialValue.price">
    </div>
     <div>
        <label for="">So luong</label>
        <br>
        <input type="number" v-model="initialValue.quantity">
    </div>
    <button  @click="handleClick">Click</button>
  </div>
</template>
<style scoped>
</style>