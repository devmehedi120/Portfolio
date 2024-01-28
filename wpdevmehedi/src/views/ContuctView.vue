<script setup>

</script>

<template >
   <section class="contactArea w-[100%] mt-[20px] pb-[10px] transition-all delay-200 ease-in-out">
    <h1 class="text-[20px] font-serif font-bold text-center md:text-[25px] lg:text-[30px] text-white">Contact Area</h1>    
    <div class=" container ">
        <form class="contuctForm flex flex-col justify-center items-center  w-[80%] md:block  font-serif  mx-auto    " action="#">
            <div class="formGroup w-[100%] mb-[10px] ">
                <label for="fullName" class="text-[15px] text-left  text-white mb-[4px] block ">Full Name</label>
                <input type="text" class=" w-[100%] outline-none bg-slate-50 border-0 focus:border-[#ddd] focus:border-[1px] px-3 py-2 rounded shadow-inner md:w-[500px] ">
            </div>            
            <div class="formGroup w-[100%]  mb-[10px] md:m-auto">
                <label for="fullName" class="text-[15px] text-left  text-white mb-[4px] block ">Your Email</label>
                <input type="email" class=" w-[100%] outline-none bg-slate-50 border-0 focus:border-[#ddd] focus:border-[1px] px-3 py-2 rounded shadow-inner md:w-[500px] ">
            </div>            
            <div class="formGroup w-[100%] mb-[10px]  md:m-auto">
                <label for="fullName" class="text-[15px] text-left  text-white mb-[4px] block ">Message</label>
                <textarea  class=" w-[100%] outline-none bg-slate-50 border-0 focus:border-[#ddd] focus:border-[1px] px-3 py-2 rounded shadow-inner md:w-[500px] " /> 
            </div>            
            <div class="formGroup  w-[100%] mb-[10px]  md:m-auto">
               <input class="bg-blue-500  mt-[10px] p-2 w-[100%] md:w-[500px] mx-auto rounded hover:bg-blue-600 text-white hover:text-orange-300 transition" type="button" value="Send ">
            </div>            
        </form>
    </div>
   </section>
</template>
<style scoped></style>
