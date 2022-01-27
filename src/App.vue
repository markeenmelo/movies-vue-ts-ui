<script setup lang="ts">
import { reactive, onMounted } from 'vue'
import MovieCard from "./components/MovieCard.vue";

const state = reactive({ movies: [] })

onMounted(() => {
  fetch('https://hackeryou-marcos-api.herokuapp.com/movies')
      .then(response => response.json())
      .then(data => state.movies = data)
})
</script>

<template>
  <h1 class="text-3xl font-bold underline">
    <MovieCard v-for="movie in state.movies" :title="movie.title" :poster="movie.poster_path" :overview="movie.overview"/>
  </h1>

</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
