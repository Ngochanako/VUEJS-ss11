<template>
  <div>
    <h2>Danh sách mục</h2>
    <div v-for="(item,index) in [...items].reverse()" :key="index">Mục mới:{{ item }}</div>
  </div>
</template>

<script setup>
import { onBeforeMount, onMounted, onUnmounted, reactive } from "vue";

let items=reactive([12345,56778445,354657757,6446575757]);
const addItem=()=>{
        items.pop();
        items.push(Math.floor(Math.random()*1000000000));
    }
onBeforeMount(()=>{
    console.log('COmponnent được gắn kết');
    
})
onMounted(()=>{
    const intervalID=setInterval(addItem,5000)
    return ()=>{
        clearInterval(intervalID);
       
    }
})
onUnmounted(()=>{
    console.log('Component đã hủy');
})
</script>

<style>

</style>