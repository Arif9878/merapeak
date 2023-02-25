<template>
  <div class="app" id="app">
    <!-- Render contents with transition -->
    <transition name="fade" mode="out-in">
      <Nuxt />
    </transition>

    <Slider />
    <div class="px-6 pb-6">
      
      <!-- Kategori Card -->
      <div class="my-2">
        <div class="flex items-center text-black font-bold justify-between">
          <p>Kategori</p>
          <i class="fa fa-chevron-down"></i>
        </div>
        <div class="card-wrapper mt-2">
          <div class="card" v-for="card in 4" :key="card">
              <Card />
          </div>
        </div>
      </div>

      <!-- Paket Card -->
      <div class="mt-2 mb-20">
        <div class="flex items-center text-black font-bold justify-between">
          <p>Paket</p>
          <i class="fa fa-chevron-down"></i>
        </div>
        <div class="card-wrapper mt-2">
          <div class="card-package" v-for="card in 4" :key="card">
            <Card />
          </div>
        </div>
      </div>
    </div>
    <Navbar />
  </div>
</template>

<script>
import feather from "feather-icons";
import Slider from "../components/Slider.vue";
import Navbar from "../components/Navbar.vue";
import Card from '../components/Card.vue'
import List from '../components/List.vue'
   
export default {
  data: () => {
    return {
      // Todo
    };
  },
  mounted() {
    feather.replace();
  },
  components: { Slider, Card, Navbar, List },
};
</script>

<style scoped>
   .text-xxs {
      font-size: .75rem;
   }
   .text-xxxs {
      font-size: .55rem;
   }
  .card {
      min-width: 52%;
      animation: card .3s ease-in-out forwards;
      @apply rounded-xl relative overflow-hidden;
   }
  .card-package {
      min-width: 40%;
      animation: card .3s ease-in-out forwards;
      @apply rounded-xl relative overflow-hidden;
   }
   .category-wrapper, .card-wrapper {
      @apply flex gap-3 overflow-scroll;
   }
   .category {
      @apply bg-gray-100 duration-300 px-3 py-1 rounded-xl text-green-500 text-xs font-medium;
   }
   .active {
      @apply bg-green-400 text-gray-50;
   }
   
</style>
