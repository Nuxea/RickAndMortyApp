<script setup>
import RickAndMortyCards from "@/components/RickAndMortyCards.vue";
import Header from "@/components/Header.vue";
import PracticeSlot from "@/components/PracticeSlot.vue";
</script>

<template>
  <main>
    <Header />
    <Suspense>
      <template #default>
        <RickAndMortyCards />
      </template>
      <template #fallback>
        <div class="cards spinner">
          <n-spin size="large" />
        </div>
      </template>

    </Suspense>
<!--    <PracticeSlot>-->
<!--      <template #header>-->
<!--        <div>-->
<!--          <h2>This is a header Slot</h2>-->
<!--        </div>-->
<!--      </template>-->
<!--      <template #body>-->
<!--        <h4>Title Slot</h4>-->
<!--        <p><span>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Amet illo in minima nesciunt omnis pariatur porro quod tempora, velit! Aspernatur eligendi est et eum fugit, perferendis qui repellat rerum voluptatibus.</span><span>Amet aperiam asperiores distinctio excepturi illo necessitatibus non, officiis perspiciatis placeat praesentium recusandae soluta tempore temporibus, vel veritatis? Ab alias aspernatur blanditiis culpa deleniti doloribus et facilis inventore odit soluta.</span><span>Ab, adipisci consequuntur deleniti dolore ducimus itaque laborum magnam modi, nostrum odio officia pariatur placeat possimus quaerat, quo unde voluptates. Deserunt est nam quos? Ducimus esse laboriosam non unde voluptatem!</span><span>Aliquid aperiam delectus eum illo molestias repudiandae sapiente! Dicta perspiciatis recusandae tenetur? Accusantium amet deleniti eaque esse et explicabo, odio suscipit ullam? Commodi esse porro quisquam repellendus. Accusantium, harum sequi.</span><span>Ab ad, at autem eum eveniet explicabo nesciunt officiis pariatur sed tempore ullam voluptatum. Cupiditate dolore eius illum, impedit, modi nihil odio odit optio perspiciatis porro repudiandae, sapiente tempora totam?</span></p>-->
<!--      </template>-->
<!--      <template #footer>-->
<!--        <small>Footer Slot</small>-->
<!--      </template>-->
<!--    </PracticeSlot>-->
  </main>
</template>

<style scoped>
.cards {
  height: 700px;
  background-color: rgb(27, 26, 26);
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
