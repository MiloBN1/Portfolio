<script setup lang="ts">

</script>

<template>
  <div class="line"></div>
</template>

<style scoped>
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