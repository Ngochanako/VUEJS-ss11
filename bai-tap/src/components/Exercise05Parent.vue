<template>
    <div>
     <Exercise05ChildrenVue v-if="show"/>
     <button @click="handleClick">Toggle</button>
    </div>
</template>

<script setup>
import { ref } from "vue";
import Exercise05ChildrenVue from "./Exercise05Children.vue";
import { onBeforeUnmount, onUnmounted } from "vue";
const show=ref(false);

const handleClick = () => {
  show.value =!show.value;
};
onBeforeUnmount(()=>{
    console.log('Component is about to be unmounted');
    
})
onUnmounted(()=>{
    console.log('Component has been unmounted');
    
})
</script>

<style>

</style>