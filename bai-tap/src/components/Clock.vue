<template>
    <div>
        <p>Thời gian hiện tại:{{ hour }}:{{ minutes }}:{{ second }}</p>
    </div>
</template>

<script setup>
import { onBeforeUnmount, onMounted ,ref} from "vue";

const hour=ref(new Date().getHours());
const minutes=ref(new Date().getMinutes());
const second=ref(new Date().getSeconds());
const getTime=()=>{
    hour.value=new Date().getHours();
    minutes.value=new Date().getMinutes();
    second.value=new Date().getSeconds();
}
console.log(second.value);

onMounted(()=>{
   const intervalID=setInterval(getTime,1000);
    return ()=>clearInterval(intervalID);  
})

</script>

<style>

</style>