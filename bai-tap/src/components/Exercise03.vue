<template>
    <div>
        <button @click="random">Random</button>
        <p>Age:{{ age }}</p>
        <p>Company:{{ company }}</p>
    </div>
</template>

<script setup>
import { ref } from "vue";

let age=ref(1);
let company=ref('Rikkei Academy');
let companies=[ "Rikkei Academy", "Rikkei Education", "Rikkei Fukuoka"];
const random=()=>{
    age.value=Math.floor(Math.random()*10);
    company.value=companies[Math.floor(Math.random()*companies.length)];
}
</script>

<style>

</style>