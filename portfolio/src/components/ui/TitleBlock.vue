<script setup lang="ts">
  let props = defineProps(['title'])
  //for build start
</script>

<template>
  <div class="bg-[#252525] px-[60px] border-b-2 border-t-2 border-[#333333] py-24 text-white main-text">
    {{ props.title }}
  </div>
</template>

<style scoped>

</style>