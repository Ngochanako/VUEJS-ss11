<template>
    <div class="flex gap-[20px]">
        <div class="light bg-green-500">
            {{ green }}
        </div>
        <div class="light bg-red-400">
            {{ red }}
        </div>
        <div class="light bg-yellow-400">
            {{ yellow }}
        </div>
    </div>
</template>

<script setup>
import { onMounted, ref } from "vue";

const green=ref(0);
const red=ref(60);
const yellow=ref(0);
const cal=()=>{
    if(red.value>0){
        red.value--;
        if(red.value==0){
            green.value=40;
        }
    }
    else if(green.value>0){
        green.value--;
        if(green.value==0){
            yellow.value=3;
        }
    }
    else if(yellow.value>0){
        yellow.value--;
        if(yellow.value==0){
            red.value=60;
        }
    }
}
onMounted(()=>{
    const intervalID=setInterval(cal,1000);
    return () => clearInterval(intervalID); 
})
</script>

<style>
.light{
  width: 100px;
  height: 100px;
  border-radius: 50%;
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>