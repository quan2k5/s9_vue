<script setup>
import {ref} from'vue'
import b1 from './components/homework/B1.vue'
import b2 from './components/homework/B2.vue'
import b3 from './components/homework/B3.vue'
import b4 from './components/homework/B4.vue'
import b5 from './components/homework/B5.vue'
import b6 from './components/homework/B6.vue'
import b7 from './components/homework/B7.vue'
import b8 from './components/homework/B8.vue'
import b9 from './components/homework/B9.vue'
import b10 from './components/homework/B10.vue'
const count=ref(0)
const handleClick=()=>{
  count.value++;
}
console.log('re-rende');

</script>r
<template>
  <div>
    <h3>session 9</h3>
    <p>1.one-way binding</p>
    <button @click='handleClick'>CLICK</button>
    <p>Hien thi gia tri count la {{count}}</p>
    <p>bai 1</p>
    <b1></b1>
    <p>bai 2</p>
    <b2></b2>
    <p>bai 3</p>
    <b3></b3>
    <p>bai 4</p>
    <b4></b4>
    <p>bai 5</p>
    <b5></b5>
    <p>bai 6</p>
    <b6></b6>
    <p>bai 7</p>
    <b7></b7>
    <p>bai 8</p>
    <b8></b8>
    <p>bai 9</p>
    <b9></b9>
    <p>bai 10</p>
    <b10></b10>
  </div>
</template>


