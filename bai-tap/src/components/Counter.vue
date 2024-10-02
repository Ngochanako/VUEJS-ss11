<template>
    <div>Count:{{ count }}</div>
</template>

<script setup>
import { onBeforeUnmount, onMounted,ref } from "vue";

const count=ref(0);

const incrementCount = () => {
    count.value++;
}
let interval;
onMounted(()=>{
  interval=setInterval(()=>{
    incrementCount();
  },1000)
})
onBeforeUnmount(()=>{
  clearInterval(interval);
})
</script>

<style>

</style>