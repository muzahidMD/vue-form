<script setup>
import { reactive, ref } from 'vue';
const displayImage = ref(true);
</script>

<template>
  <section class="mx-auto container">
    <h1 class="text-2xl mb-10">Vue Form</h1>
    <p class="mb-10">{{ displayImage }}</p>
    <label for="">Display Random Image</label>
    <input class="ml-2" type="checkbox" v-model="displayImage" />
    <img class="mt-10 mx-auto w-[500px]" v-show="displayImage"
      src="https://images.unsplash.com/photo-1744882838449-b3ad2ceff9a8?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8"
      alt="">

    <!-- v-if is more expensive -->

    <!-- <img class="mt-10 mx-auto w-[500px]" v-if="displayImage"
      src="https://images.unsplash.com/photo-1744882838449-b3ad2ceff9a8?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHw0fHx8ZW58MHx8fHx8"
      alt=""> -->

  </section>
</template>

<style scoped></style>
