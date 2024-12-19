<script setup lang="ts">
  import {ref} from "vue";

  let activePage = ref(1);

  function changeActivePage(page:number){
    activePage.value = page;
  }
</script>

<template>
  <nav class="flex justify-between items-center py-5 px-[60px] fixed left-0 right-0 top-0">
    <h1 class="main-text">Miras Baidildin</h1>
    <div>
      <a :class="activePage === 1 ? 'active' : ''" @click="changeActivePage(1)">Home</a>
      <a :class="activePage === 2 ? 'active' : ''" @click="changeActivePage(2)">Front-end skills</a>
      <a :class="activePage === 3 ? 'active' : ''" @click="changeActivePage(3)">Back-end skills</a>
      <a :class="activePage === 4 ? 'active' : ''" @click="changeActivePage(4)">Projects</a>
      <a :class="activePage === 5 ? 'active' : ''" @click="changeActivePage(5)">Contacts</a>
    </div>
  </nav>
</template>

<style scoped>
  a{
    margin-right:76px;
    color: #fff;
    opacity: 0.5;
    cursor: pointer;
  }

 .active {
    opacity: 1;
    font-weight: bold;
  }

</style>