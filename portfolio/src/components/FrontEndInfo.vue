<script setup lang="ts">

import ProgressBar from "./ui/ProgressBar.vue";
</script>

<template>
  <div >
    <div class="bg-[#252525] px-[60px] border-2 border-[#333333] py-24 text-white main-text">
      Front-end skills
    </div>
    <div class="flex px-[60px]">
      <!--   Frameworks   -->
      <div class="w-1/2 mr-24">
        <div class="f-24 mt-16">
          Frontend knowledge
          <div class="line"></div>
        </div>
        <div v-for="i in [1,2,3]" :key="i" class="flex mt-10">
          <div class="mr-8">
            <svg xmlns="http://www.w3.org/2000/svg" width="50" height="50" fill="#007CED" class="bi bi-pencil-fill" viewBox="0 0 16 16">
              <path d="M12.854.146a.5.5 0 0 0-.707 0L10.5 1.793 14.207 5.5l1.647-1.646a.5.5 0 0 0 0-.708zm.646 6.061L9.793 2.5 3.293 9H3.5a.5.5 0 0 1 .5.5v.5h.5a.5.5 0 0 1 .5.5v.5h.5a.5.5 0 0 1 .5.5v.5h.5a.5.5 0 0 1 .5.5v.207zm-7.468 7.468A.5.5 0 0 1 6 13.5V13h-.5a.5.5 0 0 1-.5-.5V12h-.5a.5.5 0 0 1-.5-.5V11h-.5a.5.5 0 0 1-.5-.5V10h-.5a.5.5 0 0 1-.175-.032l-.179.178a.5.5 0 0 0-.11.168l-2 5a.5.5 0 0 0 .65.65l5-2a.5.5 0 0 0 .168-.11z"/>
            </svg>
          </div>
          <div>
            <h3 class="text-white font-bold">
              UI / UX Design
            </h3>
            <p class="text-[#fff7]">Je obecně známou věcí, že člověk bývá při zkoumání grafického návrhu rozptylován okolním textem, pokud mu dává nějaký smysl. Úkolem Lorem Ipsum je pak nahradit klasický smysluplný text vhodnou bezvýznamovou alternativou
            </p>
          </div>
        </div>
      </div>
      <!--  Coding skills    -->
      <div class="w-1/2">
        <div class="f-24 mt-16">
          Coding skills
          <div class="line"></div>
        </div>

        <ProgressBar class="mt-8" name="HTML" percentage="100"/>
        <ProgressBar class="mt-8" name="CSS" percentage="80"/>
        <ProgressBar class="mt-8" name="JavaScript" percentage="80"/>
        <ProgressBar class="mt-8" name="TypeScript" percentage="90"/>
        <ProgressBar class="mt-8" name="React" percentage="0"/>
        <ProgressBar class="mt-8" name="Angular" percentage="90"/>
        <ProgressBar class="mt-8" name="Vue" percentage="70"/>
      </div>
    </div>
  </div>
</template>

<style scoped>
  p{
    line-height: 30px;
  }
  .line{
    width: 100px;
    height: 2px;
    background-color: #353535;
    position: relative;
  }
  .line:before{
    content: " ";
    height: 100%;
    width: 35%;
    background-color: #007CED;
    position: absolute;
    left: 0;
  }


</style>