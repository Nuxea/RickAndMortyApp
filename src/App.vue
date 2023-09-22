<script setup>
import RickAndMortyCards from "@/components/RickAndMortyCards.vue";
</script>

<template>
  <main>
    <h1>API Rick & Morty</h1>
    <Suspense>
      <template #default>
        <RickAndMortyCards />
      </template>
      <template #fallback>
        <div>
          <p>Loading...</p>
        </div>
      </template>

    </Suspense>
  </main>
</template>

<style scoped>

</style>
