<script setup lang="ts">
  import {ref} from "vue";

  let activePage = ref(0)
  const titles = ['About me', 'My XP']
  let selectedTitle = ref(titles[0])


  function changeActivePage(value:number){
    activePage.value = value;
    selectedTitle.value = titles[value]
  }

</script>

<template>
  <div class="flex justify-center items-center h-full container-main">
    <div class="circle-wrapper mr-20">
      <div class="circle">
      </div>
    </div>

    <div class="info-block w-1/3">
      <p class="opacity-text">Frontend Developer</p>
      <h1>{{ selectedTitle }}</h1>
      <p class="text-about" v-if="activePage===0">I specialize in creating web applications using Angular, React and Vue, leveraging my strong expertise in TypeScript and JavaScript. With a keen eye for detail and a passion for modern frontend development, I focus on crafting dynamic, responsive, and user-friendly interfaces.</p>
      <div v-if="activePage===1">
      <p class="text-about" >MiddleComm, 2 years <br/>
        FRONT-END ANGULAR
      </p>
        <ul class="text-white list-disc">
          <li class="ml-5"> Microservices using Express JS</li>
          <li class="ml-5"> Developing web applications with Angular 14</li>
          <li class="ml-5"> Worked with CRUD operations, used Redis for caching, and PostgreSQL for data management</li>
        </ul>
      </div>
      <div class="mt-5">
        <button class="mr-5" @click="changeActivePage(0)" :class="activePage===0?'active-btn':''">About me</button>
        <button @click="changeActivePage(1)" :class="activePage===1?'active-btn':''">My XP</button>
      </div>
    </div>
  </div>

</template>

<style scoped>
  .circle{
    width: 400px;
    height: 400px;
    border-radius: 50%;
    border:20px solid #444444;
    background-image: url("../assets/img/ProfilePhoto.jpg");
    background-size: cover;
    background-position: center top;
  }
  .opacity-text{
    font-size: 20px;
  }
  h1{
    font-size: 50px;
    color: #fff;
    font-weight: bold;
  }
  .text-about{
    color: #fff;
    font-size: 16px;
    font-weight: normal;
    line-height: 30px;
  }
  button{
    background-color: #333333;
    border: 3px solid #fff;
    padding: 15px 30px;
    border-radius: 30px;
    color: #fff;
  }
  button:hover{
    border-color: #007CED;
  }
  .active-btn{
    border-color: #007CED;
  }
  .container-main{
    height: calc(100vh - 88px)
  }
</style>