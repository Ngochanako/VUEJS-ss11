<template>
    <div>
        <p>Giá trị count:{{ count }}</p>
        <button @click="handleChange">Counter</button>
    </div>
</template>

<script setup>
import { onUpdated,ref } from "vue";

const count=ref(0);
const handleChange=()=>{
    count.value++;  
}
onUpdated(()=>{
  console.log('Dữ liệu đã thay đổi');
  
})
</script>

<style>

</style>