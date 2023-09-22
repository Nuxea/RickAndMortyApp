<script setup>
import axios from "axios";
import {ref, watch} from "vue";
import Card from "@/components/Card.vue";

const characters = ref(null)
const page = ref(1)

const response = await axios.get(`https://rickandmortyapi.com/api/character/?page=${page.value}`)
characters.value = response.data.results

watch(page, async () => {
  const response = await axios.get(`https://rickandmortyapi.com/api/character/?page=${page.value}`)
  characters.value = response.data.results
  console.log(response)
})

</script>

<template>
  <div class="container">
    <div class="cards">
      <Card
          v-for="character in characters"
          :key="character.id"
          :image="character.image"
          :name="character.name"
          :status="character.status"
          :species="character.species"
      />
    </div>
    <div class="button-container">
      <button @click="page--">&lt</button>
      <button @click="page++">></button>
    </div>
  </div>
</template>

<style scoped>
.container {
  background-color: rgb(27, 26, 26);
  width: 100%;
}
.cards {
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
}
.cards h3 {
  font-weight: bold;
}
.cards p {
  font-size: 10px;
}
.jobs {
  display: flex;
  flex-wrap: wrap;
}
.button-container {
  display: flex;
  justify-content: center;
  padding-top: 30px
}
.button-container button {
  border: none;
  width: 50px;
  height: 50px;
  border-radius: 100%;
  margin: 0 5px;
  cursor: pointer;
}
.spinner {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>