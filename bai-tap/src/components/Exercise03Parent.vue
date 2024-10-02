<template>
    <div>
        <p>Age:{{ age }}</p>
        <button @click="handleClick">Increase</button>
        <Exercise03ChildrenVue :age="age"/>
    </div>
</template>

<script setup>
import { ref } from "vue";
import Exercise03ChildrenVue from "./Exercise03Children.vue";
const age=ref(1);
const handleClick=()=>{
    age.value++  ;
}
</script>

<style>

</style>