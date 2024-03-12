<script setup>
  import {inject} from "vue";
  const { closeOrderWindow } = inject('app')

  defineProps({
    orderInfo: Array
  })
</script>

<template>
  <div class="fixed bg-black opacity-70 w-full h-full z-10"></div>
  <div class="fixed z-20 left-1/4 orderWindow">
    <div class="flex m-6 justify-between">
      <p class="goticFont text-4xl font-bold">{{ orderInfo[0][0] }}</p>
      <img src="/close.svg" alt="CloseBtn" class="cursor-pointer" @click="closeOrderWindow">
    </div>
    <div class="flex justify-center items-center flex-col">
      <img :src="orderInfo[0][1]" alt="Poster" width="440" height="440" class="mb-8 rounded-md">
      <div class="infoDiv">
        <p>Дата</p>
        <p>{{ orderInfo[0][2] }}</p>
      </div>
      <div class="infoDiv">
        <p>Цена</p>
        <p>{{ orderInfo[0][3] }} ₽</p>
      </div>
      <div class="infoDiv">
        <p>Время</p>
        <p>{{ orderInfo[0][4] }}</p>
      </div>
      <button class="orderBtnModal">Оформить заказ</button>
    </div>
  </div>
</template>

<style scoped>
  .orderWindow {
    width: 880px;
    height: auto;
    padding-bottom: 2rem;
    border-radius: 16px;
    top: 10rem;
    background-color: rgb(238, 238, 238);
  }
  .infoDiv {
    display: grid;
    grid-template-columns: repeat(2, 25rem);
    margin-bottom: 1rem;
    justify-items: center;
    align-items: center;
    font-size: 24px;
  }
  .orderBtnModal {
    background-color: #05B093;
    border-radius: 24px;
    width: 200px;
    height: 51px;
    padding: 15px 30px 14px 30px;
    color: #FFF;
  }
</style>