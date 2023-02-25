<template>
   <div class="nav-wrapper">
      <div class="navbar">
         <div v-for="(menu, index) in menus" :key="index">
            <div>
               <i :class="menu.icon" class="duration-300 text-gray-500"></i>
               <span class="duration-300 flex justify-center duration-300 flex-wrap">
                  <p class="text-xxs text-white w-full text-center">{{ menu.name }}</p>
                  <i class="text-xxxxs text-white fa fa-circle"></i>
               </span>
            </div>
         </div>
      </div>
   </div>
</template>
<script setup>
   import { ref } from 'vue'

   //List menu
   const menus = ref([
      {
         name: 'Contact us',
         icon: 'fa fa-home'
      },
      {
         name: 'FAQ',
         icon: 'fa fa-search'
      },
      {
         name: 'About us',
         icon: 'far fa-bookmark'
      },
      ])
</script>

<style scoped>
   .nav-wrapper {
      @apply fixed left-0 right-0 bottom-0;
      box-shadow: -3px 3px 12px whitesmoke;
   }
   .navbar {
      @apply duration-300 w-full md:w-8/12 lg:w-4/12 mx-auto px-6 py-4 bg-primary-dark flex justify-between;
   }
</style>