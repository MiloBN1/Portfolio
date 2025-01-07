<script setup lang="ts">

import TitleBlock from "./ui/TitleBlock.vue";
import MainLine from "./ui/MainLine.vue";

const images = [
  new URL('../assets/img/VUE-PROJECT.png', import.meta.url).href,
  new URL('../assets/img/REACT-PROJECT.png', import.meta.url).href,
  new URL('../assets/img/ANGULAR-PROJECT.png', import.meta.url).href,
];

</script>

<template>
  <TitleBlock title="Projects"/>

  <div class="px-[60px] py-16">
    <div>
      <h3 class="f-24">Vercel</h3>
      <MainLine/>
    </div>
    <div class="mt-5">
      <button class="opacity-text mr-10">Vue</button>
      <button class="opacity-text mr-10">Angular</button>
      <button class="opacity-text">React</button>
    </div>
    <div class="mt-5 flex">
      <div
          v-for="(image, index) in images"
          :key="index"
          class="w-1/3 images mr-5"
          :style="{ backgroundImage: `url(${image})` }"
      >
        <div class="view-project"><button class="btn">View Project</button></div>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .images{
    border: 2px solid #9ca3af;
    border-radius: 10px;
    height: 250px;
    background-size: cover;
    background-image: url("../assets/img/VUE-PROJECT.png");
    position: relative;
  }
  .view-project{
    position: absolute;
    inset:0;
    background-color: #0009;
    display: none;
    justify-content: center;
    border-radius: 10px;
    align-items: center;
  }
  .images:hover > .view-project{
      display: flex;
  }
  .btn{
    color: #fff;
    border: 1px solid #fff;
    padding: 10px;
    border-radius: 10px;
    transition: all .3s ease-in-out;
  }
  .btn:hover{
    color: #000;
    background-color: #fff;
  }
</style>