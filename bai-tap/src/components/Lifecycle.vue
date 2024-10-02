<template>
    <div>
        <h1>component lifecycle</h1>
        <p>{{ sayHello() }}</p>
    </div>
</template>

<script setup>
import {onBeforeMount,onBeforeUpdate,onMounted} from 'vue'
onBeforeMount(()=>{
    console.log('onbefore mount được gọi');
    
})
const sayHello=()=>{
    console.log('hello');   
}
onMounted(()=>{
  console.log('on mounted được gọi');
})
onBeforeMount(()=>{
    console.log('on before mount');   
})
onBeforeUpdate(()=>{
   console.log('on before update');   
})
</script>

<style>

</style>