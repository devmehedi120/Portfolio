<script setup>
import { ref } from 'vue';
const serviceData=ref(
    [
        {
            'icon': 'fa-brands fa-wordpress',
            'title': 'Wordpress Development',
            'description': 'I am a professionnal Wordpress Developer. I am expert with wordpress custom theme , custom plugin  development',

        },
        {
            'icon': 'fa-solid fa-palette',
            'title': 'Web Design',
            'description': 'I am a professionnal Wordpress Developer. I am expert with wordpress custom theme , custom plugin  development',

        },
        {
            'icon': 'fa-brands fa-html5',
            'title': 'HTML Service',
            'description': 'I am a professionnal Wordpress Developer. I am expert with wordpress custom theme , custom plugin  development',

        },
        {
            'icon': 'fa-solid fa-code',
            'title': 'Web Programing',
            'description': 'I am a professionnal Wordpress Developer. I am expert with wordpress custom theme , custom plugin  development',

        },
        {
            'icon': 'fa-brands fa-vuejs',
            'title': 'Development With VueJs',
            'description': 'I am a professionnal Wordpress Developer. I am expert with wordpress custom theme , custom plugin  development',

        },
        {
            'icon': 'fa-brands fa-react',
            'title': 'React UI Design',
            'description': 'I am a professionnal Wordpress Developer. I am expert with wordpress custom theme , custom plugin  development',

        },
        {
            'icon': 'fa-brands fa-node-js',
            'title': 'Node-JS Development',
            'description': 'I am a professionnal Wordpress Developer. I am expert with wordpress custom theme , custom plugin  development',

        },
        {
            'icon': 'fa-brands fa-php',
            'title': 'Custom PHP Development',
            'description': 'I am a professionnal Wordpress Developer. I am expert with wordpress custom theme , custom plugin  development',

        },
    ]
)

</script>

<template>
  <section class="serviceSection   ">
    <h1 class="text-[20px] font-serif font-bold text-center md:text-[25px] lg:text-[30px] text-white">Service Area</h1>
    <div class="servicess p-[10px]  flex justify-between flex-wrap text-white   " >
        <div class="wordpresDevelopment w-[48%] flex flex-col items-center  mb-4 border-orange-300 border-[1px] p-2 backdrop-blur-sm bg-[rgba(110,24,24,0.27)] rounded  shadow-sm md:w-[32%]  lg:w-[24%] xl:w-[19%]    cursor-pointer" v-for="(service, index) in serviceData" :key="index">
           
            <i class="text-[50px] block m-auto w-[100%]  text-center text-orange-500" :class="service.icon"></i>
                           
           <h1 class="text-[15px] font-bold   text-center tracking-normal">{{ service.title }}</h1>
            <p class="text-[12px] text-wrap text-center tracking-normal font-normal font-sans"> {{ service.description }}</p>
            <a href="" class="bg-blue-400 py-[4px] px-[7px] w-[70%] mt-[6px] rounded-md text-white  text-center hover:bg-blue-600 hover:text-orange-400 transition delay-75 ease-in-out block m-auto">Visit Here</a>

        </div>
       
      </div></section>
</template>
<style scoped>


</style>
