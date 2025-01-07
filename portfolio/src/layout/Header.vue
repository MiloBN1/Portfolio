<script setup lang="ts">
  import {ref} from "vue";

  let activePage = ref(1);

  const pages = [
    {
      id:1,
      title:"Home",
      hash:"#home"
    },
    {
      id:2,
      title:"Skills",
      hash:"#skills"
    },
    {
      id:3,
      title:"Projects",
      hash:"#projects"
    },
    {
      id:4,
      title:"Contacts",
      hash:"#contacts"
    },
  ]

  function changeActivePage(page:number){
    activePage.value = page;
  }
</script>

<template>
  <nav class="flex justify-between items-center py-5 px-[60px] fixed left-0 right-0 top-0 bg-[#222222] z-50">
    <h1 class="main-text">Miras Baidildin</h1>
    <div>
      <router-link v-for="page in pages" :key="page.id" :to="{ path: '/', hash: page.hash }" :class="activePage === page.id ? 'active' : ''" @click="changeActivePage(page.id)">
        {{ page.title }}</router-link>
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