<template>
  <!-- component -->
  <div class=" rounded overflow-hidden border w-full lg:w-6/12 md:w-6/12 bg-white mx-3 md:mx-0 lg:mx-0">
    <div class="w-full flex justify-between p-3">
      <div class="flex">
        <span class="pt-1 ml-2 font-bold text-sm">{{ props.title }}</span>
      </div>
      <span class="px-2 hover:bg-gray-300 cursor-pointer rounded"><i class="fas fa-ellipsis-h pt-2 text-lg"></i></span>
    </div>
    <img class="w-full bg-cover" :src=props.poster alt="Movie poster">
    <div class="px-3 pb-2">
      <div class="pt-1">
        <div class="mb-2 text-sm">{{ props.overview }}</div>
      </div>
      <div class="mb-2">
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'

let props = defineProps({
  title: String,
  releaseDate: Number,
  overview: String,
  poster: String,
  rate: Number
})

</script>

<style scoped>

</style>
