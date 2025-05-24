<template>
  <div class="min-h-screen text-white relative overflow-hidden">
    <!-- Fondo SVG en la mitad superior vertical -->
    <div
      class="absolute top-0 left-0 w-full h-1/2 bg-no-repeat bg-cover bg-top"
      style="background-image: url('/bg.svg');"
    ></div>

    <!-- Contenido de la app, con padding para que no quede tapado por el fondo -->
    <div class="relative z-10 px-8">
      <!-- Navbar -->
      <Header />

      <!-- Hero Section -->
      <main class="py-20 text-center max-w-4xl mx-auto">
        <h1 class="text-4xl font-bold mb-4">
          Identify <span class="text-[#176B74]">Every Visitor</span> 
        </h1>
        <p class="text-lg text-white mb-6 max-w-xl mx-auto">
          Stop fraud, detect bots, or delight customers. Identify good and bad visitors with industry-leading accuracy - even if they're anonymous.
        </p>
        <a href="#" 
           class="border border-orange-600 text-[#176B74] px-4 py-2 rounded hover:bg-orange-50 transition whitespace-nowrap">
          Get started
        </a>
        <a href="#" 
           class="ml-4 bg-orange-600 text-white px-4 py-2 rounded whitespace-nowrap">
          Contact Sales
        </a>
        <br>
        <br>
        <br>
        <br>
        <br>
        <br>
        <br>
        <br>
        <Cuerpo />
      </main>

      <!-- Modal -->
      <div v-if="showModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50">
        <div class="bg-white rounded-lg p-6 w-full max-w-md">
          <h2 class="text-xl font-semibold mb-4">Modal Title</h2>
          <p>This is a sample modal UI like Fingerprint's website.</p>
          <div class="mt-4 text-right">
            <button @click="showModal = false" class="px-4 py-2 bg-gray-200 hover:bg-gray-300 rounded">Close</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import Header from './components/Header.vue';
import Tabla from './components/Tabla.vue';
import Cuerpo from './components/Cuerpo.vue';
export default {
  components: 
  { Header, 
    Tabla,
    Cuerpo
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
