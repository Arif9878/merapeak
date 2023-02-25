<template>
   <!-- Card -->
   <div>
      <img src="../assets/mount.jpeg" />
      <div class="card-footer">
         <div 
         class="flex flex-wrap">
            <strong class="text-xxxs mb-0 w-full">Mt. Rinjani</strong>
            <p class="text-xxxxs text-gray-400">Lombok, Indonesia</p>
         </div>
         <i
         @click="isHeartClick = !isHeartClick"
         :class="isHeartClick ? 'fas' : 'far'"
         class="fa-heart duration-300 text-xs text-green-500"></i>
      </div>
   </div>
</template>

<script setup>
   import { ref } from 'vue'
   
   //Handler for Heart icon
   const isHeartClick = ref(false)
</script>

<style scoped>
   .card-footer {
      @apply absolute bottom-2 left-2 right-2 rounded-xl px-3 py-2 bg-gray-50 flex items-start gap-1;
   }
   
   @keyframes card {
      from {
         transform: translateX(-150%) scale(.75);
      } to {
         transform: translateX(0) scale(1);
      }
   } 
</style>