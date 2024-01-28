<script setup>
import { onMounted } from 'vue'
import { RouterLink, RouterView } from 'vue-router'

onMounted(() => {
    const toggleBar = document.querySelector('.toggleMenu');
    const menuItem = document.querySelector('.menuItem');

    if (toggleBar) {
        toggleBar.addEventListener('click', () => {
            menuItem.classList.toggle('top-10');
        });
    }
});
</script>


<template>
    <header class="  backdrop-blur-sm bg-transparent  w-full fixed top-0 z-10">
        <nav
            class="   container   m-auto min-h-[50px] flex md:items-center md:flex-row flex-col   md:justify-between w-full  px-[10px] py-[15px]  relative">
            <div class="logo  md:w-1/4">
                <RouterLink class="text-l  text-left  font-serif font-bold text-[aqua]  px-1 py-1 md:text-center" to="/">WP
                    MEHEDI</RouterLink>
            </div>
            <ul class=" menuItem block m-auto md:mx-auto md:w-[75%] list-none absolute md:static   top-[-400px] transition-all ease-in text-white transform bg-transparent backdrop-blur-sm w-[100%] left-0  text-center  hover:*:text-[#fad96b] font-serif ">
                <li class="  block mx-auto  text-center md:inline  mr-4 ">
                    <RouterLink class="  " to="/">Home</RouterLink>
                </li>
                <li class="  block mx-auto  text-center md:inline mr-4">
                     <RouterLink class="" to="/about">About</RouterLink>
                </li >
                <li class="  block mx-auto  text-center md:inline mr-4 ">
                      <RouterLink class="" to="/service">Service
                    </RouterLink>
                </li>
                <li class="  block mx-auto  mb-[10px] text-center md:inline mr-4">
                    
                    <RouterLink class=" " to="/contuct">Contact
                    </RouterLink>
                </li>
            </ul>
           
        </nav>

        <i class="fa-solid fa-bars absolute top-[15px] right-[20px] text-[#fff]  md:before:hidden toggleMenu"></i>

    </header>

    <div class="container m-auto mt-[100px] md:mt-[50px]">
        <!-- Use the new slot-based syntax for RouterView -->
        <router-view  v-slot="{ Component }">
            <transition name="fade" mode="out-in">
                <component :is="Component" />
            </transition>
        </router-view>
    </div>
</template>

<style scoped>
.fade-enter-active,
.fade-leave-active {
    transition: opacity 0.4s;
}

.fade-enter,
.fade-leave-to {
    opacity: 0;
}

/* we will explain what these classes do next! */

/* Define the transition for the 'hidden' class */
.navMenu {
    transition: opacity 0.4s ease, transform 0.3s ease;
}

/* Apply styles when the 'hidden' class is present */
.navMenu.hidden {
    opacity: 0;
    transform: translateY(-20px);
}</style>
