<script setup>
import { reactive } from 'vue';

const person = reactive({
  Name: 'Momin Khan',
  Age: 25,
  Job: 'Web Developer'
})

</script>

<template>
  <section class="bg-gray-300 w-full h-screen">
    <div class="mx-auto text-center pt-[250px]">
      <h1 class="text-2xl font-bold">Vue Form</h1>
      <p class="mb-10 mt-10 text-2xl"> <span class="text-red-400">{{ person }}</span></p>
      <div class="flex justify-center items-center mb-5" v-for="(value, key, index) in person" :key="index">
        <label class="font-bold mr-5 align-left">{{ key }}: </label>
        <input class="w-1/4 border-none bg-slate-200" type="text" v-model="person[key]">
      </div>
    </div>
  </section>
</template>


<style scoped></style>
