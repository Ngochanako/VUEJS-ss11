<template>
   <div>
      <input v-model="value" type="text">
   </div>
</template>

<script setup>
import { ref, watch } from "vue";

const value=ref('')
watch(value, (newCount) => {
  document.title = `${newCount}`;
});
</script>

<style>

</style>