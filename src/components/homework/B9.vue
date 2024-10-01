<script setup>
import {ref,reactive} from 'vue'
let users=reactive(JSON.parse(localStorage.getItem('users'))||[])
const intialUser= reactive({
    name:'',
    email:'',
    password:'',
    address:'',
})
const validateUser=()=>{
    if(intialUser.name===''||intialUser.email===''||intialUser.password===''){     
        return false;
    }
    let find=users.find((item)=>{
        return item.email===intialUser.email
    })
    if(find){
        return false;
    }
    return true;
}
const reset=()=>{
    intialUser.name='';
    intialUser.email='';
    intialUser.password='';
    intialUser.address='';
}
const handleClick=()=>{
    if( validateUser()){
    users.push(intialUser);
    localStorage.setItem("users",JSON.stringify(users));
    reset();
    }else{
        alert('du lieu nhap vao ko hop le');
    }
}
</script>
<template>
<div>
    <h4>Dang ky tai khoan</h4>
    <div>
        <label for="">Name</label>
        <br>
        <input type="text" v-model="intialUser.name">
    </div>
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
    <div>
        <label for="">dia chi</label>
        <br>
        <input type="text" v-model="intialUser.address">
    </div>
    <button @click="handleClick">Dang ky</button>
</div>
</template>
<style scoped>
</style>