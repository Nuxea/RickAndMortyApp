<script setup>
import axios from "axios";

const response = await axios.get('https://rickandmortyapi.com/api/character')

</script>

<template>
  <div>
    <h1>Rick & Morty Cards</h1>
  </div>
</template>

<style scoped>

</style>