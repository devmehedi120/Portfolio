<script setup>
import { onMounted } from 'vue'
import { RouterLink, RouterView } from 'vue-router'

onMounted(() => {
  const toggleBar = document.querySelector('.toggleMenu');
  const menuItem = document.querySelector('.menuItem');

  if (toggleBar) {
    toggleBar.addEventListener('click', () => {
      menuItem.classList.toggle('hidden');
    });
  }
});
</script>


<template>
  <header class="relative container bg-[#0000007a] backdrop-blur-sm m-auto">
      <nav class=" min-h-[50px] flex md:items-center md:flex-row flex-col  gap-y-[5px]  md:justify-between w-full  px-[10px] py-[15px]">
        <div class="logo  md:w-1/4">
          <RouterLink class="text-l  text-left  font-serif font-bold text-[aqua]  px-1 py-1 md:text-center" to="/">WP MEHEDI</RouterLink>
        </div>
        <div class="navMenu sticky  flex flex-col hover:*:text-[#fad96b]   md:flex-row md:items-center w-3/4 justify-center  menuItem ">
          <RouterLink class=" text-center  text-[#fff]  md:mr-[20px] mb-[10px] md:mb-0 " to="/">Home</RouterLink>
          <RouterLink class="text-center text-[#fff] md:mr-[20px] mb-[10px] md:mb-0" to="/about">About</RouterLink>
          <RouterLink class="text-center text-[#fff] md:mr-[20px] mb-[10px] md:mb-0" to="/service">Service</RouterLink>
          <RouterLink class="text-center text-[#fff] md:mr-[20px] mb-[10px] md:mb-0" to="/contuct">Contact</RouterLink>
        </div>
      </nav>  

       <i class="fa-solid fa-bars absolute top-[15px] right-[20px] text-[#fff]  md:before:hidden toggleMenu"></i>
  </header>

  <div class="container m-auto">
    <RouterView />
  </div>
</template>

<style scoped>
/* Define the transition for the 'hidden' class */
.navMenu {
  transition: opacity 0.4s ease, transform 0.3s ease;
}

/* Apply styles when the 'hidden' class is present */
.navMenu.hidden {
  opacity: 0;
  transform: translateY(-20px);
}


</style>
