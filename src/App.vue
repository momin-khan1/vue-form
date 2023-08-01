<script setup>
import { ref } from 'vue';

const displayImage = ref(true)

</script>

<template>
  <section class="bg-gray-300 w-full h-screen">
    <div class="mx-auto text-center pt-[150px]">
      <h1 class="text-2xl font-bold">Vue Form</h1>
      <p class="mb-10 mt-10 text-2xl"> <span class="text-red-400">{{ displayImage }}</span></p>
      <label class="text-xl mr-5">Display Random Image</label>
      <input type="checkbox" v-model="displayImage">
      <p class="mt-5">
        <input type="radio" v-model="displayImage" :value="true"> On <br />
        <input type="radio" v-model="displayImage" :value="false"> Off <br />
      </p>
      <img v-show="displayImage" class="w-[440px] h-[400px] mx-auto mt-10"
        :src="`https://source.unsplash.com/random?version=${Math.random()}`" alt="">
    </div>
  </section>
</template>


<style scoped></style>
