<script setup>
import {ref,reactive} from 'vue'
let users=reactive(JSON.parse(localStorage.getItem('users'))||[])
const intialUser= reactive({
    email:'',
    password:'',
})
const validateUser=()=>{
    let find=users.find((item)=>{
        return item.email===intialUser.email;
    })
    if(find){
        if(find.password==intialUser.password){
            return true;
        }
        return false;
    }
    return false;

}
const reset=()=>{
    intialUser.email='';
    intialUser.password='';   
}
const handleClick=()=>{
    if( validateUser()){
    alert('Dang nhap thanh cong')
      reset();
    }else{
        alert('khong tim thay tai khoan');
    }
}
</script>
<template>
<div>
    <h4>Dang nhap tai khoan</h4>
    <div>
        <label for="">email</label>
        <br>
        <input type="email" v-model="intialUser.email">
    </div>
    <div>
        <label for="">mat khau</label>
        <br>
        <input type="password" v-model="intialUser.password">
    </div>
    <button @click="handleClick">Dang nhap</button>
</div>
</template>
<style scoped>
</style>