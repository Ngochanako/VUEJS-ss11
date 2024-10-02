<template>
    <div>
        <p>Count:{{ count }}</p>
        <button @click="handleClick">Increment</button>
    </div>
</template>

<script setup>
import { ref, watch } from "vue";

const count=ref(1);
const handleClick=()=>{
    count.value++; 
}
watch(count, (newCount) => {
  document.title = `${newCount}`;
});
</script>

<style>

</style>