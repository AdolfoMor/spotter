<template>
  <div class="min-h-screen text-white relative overflow-hidden">
    <!-- Fondo SVG -->
    <div
      class="absolute top-0 left-0 w-full h-1/2 bg-no-repeat bg-cover bg-top"
      style="background-image: url('/bg.svg');"
    ></div>
    <Header />  
    <!-- Contenido -->
    <div class="relative z-10 px-2 sm:px-4 md:px-6">
      <!-- Navbar -->
      

      <!-- Hero Section -->
      <main class="py-20 text-center max-w-6xl mx-auto">
        <h1 class="text-4xl font-bold mb-4">
          Get more out of each mile with <span class="text-[#176B74]">spotter</span>
        </h1>
        <p class="text-lg text-white mb-6 max-w-xl mx-auto">
          AI technology that gets you hot loads.
        </p>
        <div class="flex flex-col sm:flex-row justify-center items-center gap-4">
          <a href="#" 
             class="border border-[#176B74] text-[#176B74] px-4 py-2 rounded bg-white hover:bg-white hover:bg-opacity-10 transition whitespace-nowrap">
            Get started
          </a>
          <a href="#" 
             class="bg-[#176B74] text-white px-4 py-2 rounded whitespace-nowrap">
            Contact Sales
          </a>
        </div>

        <div class="mt-10">
          <Cuerpo />
        </div>
      </main>

      <!-- Modal -->
      <div v-if="showModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50">
        <div class="bg-white rounded-lg p-6 w-full max-w-md">
          <h2 class="text-xl font-semibold mb-4 text-black">Modal Title</h2>
          <p class="text-black">This is a sample modal UI like Fingerprint's website.</p>
          <div class="mt-4 text-right">
            <button @click="showModal = false" class="px-4 py-2 bg-gray-200 hover:bg-gray-300 rounded text-sm">Close</button>
          </div>
        </div>
      </div>
    </div>
  </div>
  <Flotante />
</template>




<script>
import Header from './components/Header.vue';
import Tabla from './components/Tabla.vue';
import Cuerpo from './components/Cuerpo.vue';
import Flotante from './components/Flotante.vue';
export default {
  components: 
  { Header, 
    Tabla,
    Cuerpo,
    Flotante
  },
  data() {
    return {
      showMenu: false,
      showModal: false,
      windowWidth: window.innerWidth,
    };
  },

};
</script>
