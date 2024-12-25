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
  <div class="flex justify-center items-center h-full">
    <div class="circle-wrapper mr-20">
      <div class="circle">
      </div>
    </div>

    <div class="info-block w-1/3">
      <p class="opacity-text">Fullstack Developer</p>
      <h1>{{ selectedTitle }}</h1>
      <p class="text-about" v-if="activePage===0">Hello, my name is Miras Baidildin. I create web applications using Angular and Vue. I work with TypeScript, JavaScript, and Python and build backends with Django Rest Framework or Node.js frameworks like Nest.js and Express.js. My skills enable me to deliver full-stack solutions tailored to any project.</p>
      <div v-if="activePage===1">
      <p class="text-about" >MiddleComm, 2 years <br/>
        FRONT-END ANGULAR
      </p>
        <ul class="text-white list-disc ">
          <li class="ml-5"> Микросервисы с помощью Express JS</li>
          <li class="ml-5"> Разработка веб-приложении с использованием Angular 14</li>
          <li class="ml-5"> Работал с CRUD-операциями, использовал Redis для кэширования и
            базы данных PostgreSQL для управления данными</li>
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
</style>