<script setup>
import Calculator from './components/Calculator.vue';
import AnimeQuote from './components/AnimeQuote.vue';
</script>

<template>
  <div class="max-w-2xl mx-auto">
    <div class="text-center mt-10 mb-10 border-[1px] border-black-400 px-5 py-10 rounded">
        <h1 class="text-3xl font-bold mb-5 text-center bg-blue-500 text-white rounded p-2">Calculator</h1>
        <Calculator />
    </div>
    <div class="text-center mt-10 mb-10 border-[1px] border-black-400 px-5 py-10 rounded">
      <h1 class="text-3xl font-bold mb-5 text-center bg-blue-500 text-white rounded p-2">Random Anime Quote</h1>
      <AnimeQuote />
    </div>
  </div>
</template>

<style scoped>

</style>
