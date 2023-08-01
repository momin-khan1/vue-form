<script setup>
import { ref } from 'vue';

const color = ref('None')

const getColor = () => {
  return{
    backgroundColor: color.value
  }
}

</script>

<template>
  <section class="bg-gray-300 w-full h-screen">
    <div class="mx-auto text-center pt-[250px]">
      <h1 class="text-2xl font-bold">Vue Form</h1>
      <p class="mb-10 mt-10 text-2xl">Your Favorite Color: <span class="text-red-400">{{ color }}</span></p>
      <input class="w-1/4 border-none bg-slate-200" type="text" v-model="color">
    </div>
    <div class="mt-10 w-40 h-40 mx-auto" :style="getColor()"></div>
  </section>
</template>


<style scoped></style>
