<template>
  <div class="min-h-screen bg-neutral-50 text-gray-900">
    <!-- Navbar -->

    <Header />

    <!-- Hero Section -->
    <main class="py-20 text-center">
      <h1 class="text-4xl font-bold mb-4">
        The internet's most <span class="text-orange-600">accurate</span> visitor identifier
      </h1>
      <p class="text-lg text-gray-600 mb-6 max-w-xl mx-auto">
        Industry-leading accuracy that lasts for months or years, even when cookies are cleared.
      </p>
      <button class="bg-orange-600 hover:bg-orange-700 text-white px-6 py-2 rounded">
        Learn More
      </button>
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
