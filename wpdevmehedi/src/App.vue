<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
  <header>
      <nav class=" flex md:flex-row flex-col  gap-y-[5px] bg-[#0000007a] backdrop-blur-sm md:justify-between w-full  px-[10px] py-[15px]">
        <div class="logo  md:w-1/4">
          <RouterLink class="text-l  text-left font-serif font-bold text-[aqua]  px-1 py-1 md:text-center" to="/">WP MEHEDI</RouterLink>
        </div>
        <div class="navMenu flex flex-col hover:*:text-[#fad96b] md:flex-row  ">
          <RouterLink class=" text-center text-[#fff]  md:mr-[10px] " to="/">Home</RouterLink>
          <RouterLink class="text-center text-[#fff] md:mr-[10px]" to="/about">About</RouterLink>
          <RouterLink class="text-center text-[#fff] md:mr-[10px]" to="/service">Service</RouterLink>
          <RouterLink class="text-center text-[#fff] md:mr-[10px]" to="/contuct">Contact</RouterLink>
        </div>
      </nav>    
  </header>

  <RouterView />
</template>

<style scoped>

</style>
