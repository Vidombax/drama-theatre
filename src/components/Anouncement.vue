<script setup>
  defineProps({
    data: String,
    title: String
  })
</script>

<template>
  <div class="anouncement-item">
    <p class="text-2xl goticFont font-bold w-20 text-center">{{ data }}</p>
    <p>{{ title }}</p>
  </div>
</template>

<style>
  .anouncement-item {
    display: grid;
    grid-template-columns: 6.4rem 11rem;
    font-weight: 500;
    align-items: center;
    cursor: pointer;
    font-size: smaller;
  }
  .anouncement-item p:first-child {
    background-color: rgba(5, 176, 147, 1);
    color: #FFFFFF;
    border-radius: 8px;
    padding: 8px;
  }
</style>