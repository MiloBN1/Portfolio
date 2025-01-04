<script setup lang="ts">
import frontJson from "../shared/jsons/Front-skills.json"
import ProgressBar from "./ui/ProgressBar.vue";
import TitleBlock from "./ui/TitleBlock.vue";
import MainLine from "./ui/MainLine.vue";


</script>

<template>
  <div >
    <TitleBlock title="Frontend skills"/>
    <div class="flex px-[60px] pb-16">
      <!--   Frameworks   -->
      <div class="w-1/2 mr-24">
        <div class="f-24 mt-16">
          Frontend knowledge
          <MainLine/>
        </div>
        <div v-for="i in frontJson" :key="i.id" class="flex mt-10">
          <div class="mr-8 text-4xl text-[#007CED]">
            <i :class="i.icon"></i>
          </div>
          <div>
            <h3 class="text-white font-bold">
              {{i.title}}
            </h3>
            <p class="text-[#fff7]">{{i.description}}</p>
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
        <ProgressBar class="mt-8" name="React" percentage="70"/>
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
</style>