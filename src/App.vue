<script setup>
import { reactive, ref } from 'vue';
const person = reactive({
  name: "Muzahidul Islam",
  age: 25,
  job: "web developer",
})
</script>

<template>
  <section class="mx-auto container">
    <h1 class="text-2xl mb-10">Vue Form</h1>
    <p class="mb-10">{{ person }} </p>

    <!-- <div class="w-32 h-32 mt-10">
      <label for="name">Name</label>
      <input type="text" class="border border-gray-300 rounded-md p-2" v-model="person.name">
      <input type="text" class="border border-gray-300 rounded-md p-2" v-model="person.age">
      <input type="text" class="border border-gray-300 rounded-md p-2" v-model="person.job">
    </div> -->
    <div class="w-32 h-32 mt-10" v-for="(value, key, index) in person" :key="index">
      <label for="name">{{ key }}</label>
      <input type="text" class="border border-gray-300 rounded-md p-2" v-model="person[key]">
    </div>


  </section>
</template>

<style scoped></style>
