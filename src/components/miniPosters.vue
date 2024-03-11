<script setup>
  defineProps({
    Image: String,
    Name: String
  })
</script>
<template>
  <div class="flex items-center miniAfisha">
    <img :src="Image" alt="Opera" class="miniAfishaImg">
    <p>{{ Name }}</p>
  </div>
</template>