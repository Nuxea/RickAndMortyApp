<script setup>
import {defineProps} from "vue"

const {image, name, status, species} = defineProps([
  'image',
  'name',
  'status',
  'species'
])
</script>

<template>
  <div class="containerCard">
    <img :src="image" alt="">
    <div class="textContainer">
      <h3>{{ name }}</h3>
      <span><small>{{ status }} - {{ species }}</small></span>
      <slot></slot>
    </div>
  </div>

<!--  <NCard>-->
<!--    <template>-->
<!--      <img :src="image" alt="">-->
<!--    </template>-->
<!--    <h3>{{ name }}</h3>-->
<!--    <div class="type">-->
<!--      <p>-->
<!--        {{species}}-->
<!--      </p>-->
<!--    </div>-->
<!--  </NCard>-->
</template>

<style scoped>
.containerCard {
  display: flex;
  width: 380px;
  margin: 10px;
}

.containerCard img {
  width: 150px;
  border-radius: 15px 0 0 15px;
}

.textContainer {
  width: 250px;
  border-radius: 0 15px 15px 0;
  background-color: #3b3b3b;
  display: flex;
  flex-direction: column;
  padding: 15px;
}
</style>