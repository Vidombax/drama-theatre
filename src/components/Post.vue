<script setup>
  defineProps({
    Image: String,
    NamePost: String,
    AboutPost: String
  })
</script>
<template>
  <div class="grid grid-cols-2 post">
    <div class="flex justify-center flex-col">
      <img :src="Image" alt="News" class="mb-8" width="306" height="204">
      <p class="text-3xl font-bold goticFont mb-8">{{ NamePost }}</p>
      <p class="text-xl day">{{ AboutPost }}</p>
    </div>
  </div>
</template>

<style scoped>
  .post {
    width: 702px;
    height: 394px;
  }
</style>