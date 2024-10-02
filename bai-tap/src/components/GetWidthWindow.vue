<template>
     <h1>Chiều rộng cửa sổ: {{ windowWidth }} px</h1>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue';
const windowWidth = ref(window.innerWidth);

// Hàm để cập nhật chiều rộng cửa sổ
const updateWindowWidth = () => {
  windowWidth.value = window.innerWidth;
};
onMounted(() => {
  window.addEventListener('resize', updateWindowWidth); 
});
onBeforeUnmount(() => {
  window.removeEventListener('resize', updateWindowWidth); 
});
</script>

<style>

</style>