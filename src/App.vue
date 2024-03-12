<script setup>
  import Header from './components/Header.vue'
  import Main from './components/Main.vue'
  import Footer from './components/Footer.vue'
  import OrderWindow from "./components/OrderWindow.vue";
  import {provide, ref} from "vue";
  import {testFunc} from './routes/index.js';

  const orderWindowOpen = ref(false)
  const orderInfo = ref([])

  const closeOrderWindow = () => {
    orderWindowOpen.value = false
  }
  const openOrderWindow = (item) => {
    orderWindowOpen.value = true
    orderInfo.value = []
    orderInfo.value.push(item)
    console.log(orderInfo)
  }

  provide('app', {
    closeOrderWindow,
    openOrderWindow
  })
</script>

<template>
  <OrderWindow v-if="orderWindowOpen" :order-info="orderInfo"/>
  <header>
    <Header />
  </header>

  <main>
    <Main />
  </main>

  <footer>
    <Footer />
  </footer>
</template>

<style scoped>
  footer {
    background-color: #191919;
    padding-bottom: 2rem;
  }  
</style>
