<script setup lang="ts">
import Header from "./layout/Header.vue";
import Footer from "./layout/Footer.vue";
</script>

<template>
  <div class="h-[88px]">
    <Header></Header>
  </div>
  <div class="container-fluid">
    <RouterView />
  </div>
  <Footer></Footer>
</template>

<style scoped>
  .container-fluid{
    height: calc(100vh - 88px - 66px);
  }
</style>
