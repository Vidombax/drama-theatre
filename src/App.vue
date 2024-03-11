<script setup>
  import Header from './components/Header.vue'
  import Main from './components/Main.vue'
  import Footer from './components/Footer.vue'
  import OrderWindow from "./components/OrderWindow.vue";
  import {provide, ref} from "vue";

  const orderWindowOpen = ref(false)

  const closeOrderWindow = () => {
    orderWindowOpen.value = false
  }
  const openOrderWindow = () => {
    orderWindowOpen.value = true
  }

  provide('app', {
    closeOrderWindow,
    openOrderWindow
  })
</script>

<template>
  <OrderWindow v-if="orderWindowOpen"/>
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
