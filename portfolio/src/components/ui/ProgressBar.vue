<script setup lang="ts">
  const props = defineProps(['percentage', 'name'])
</script>

<template>
  <div>
    <div class="flex justify-between text-white font-bold">{{ props.name }} <span class="text-[#fff7] font-normal">{{props.percentage}}%</span></div>
    <div class="progress-bar" :style="`--progress-width: ${props.percentage}%`"></div>
  </div>
</template>

<style scoped>
.progress-bar{
  width: 100%;
  height: 11px;
  border-radius: 8px;
  border:3px solid #444444;
  position: relative;
  --progress-width: 0%;
}

.progress-bar:before{
  content: " ";
  height: 100%;
  background-color: #007CED;
  position: absolute;
  border-radius: 8px;
  left: 0;
  width: var(--progress-width);
}

</style>