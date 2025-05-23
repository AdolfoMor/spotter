<template>

    <header class="bg-white shadow-sm sticky top-0 z-10">
    <div class="max-w-7xl mx-auto px-4 py-3 flex items-center justify-between relative text-sm">

      <!-- Logo a la izquierda -->
      <div class="text-lg font-bold text-orange-600 flex-shrink-0">
        🌀 FingerVue
      </div>

      <!-- Botones centrales centrados absolutamente solo en lg -->
      <nav
        class="hidden lg:flex space-x-6 absolute left-1/2 top-1/2 transform -translate-x-1/2 -translate-y-1/2"
      >
        <a href="#" class="text-gray-700 hover:text-orange-600 whitespace-nowrap">Product</a>
        <a href="#" class="text-gray-700 hover:text-orange-600 whitespace-nowrap">Use Cases</a>
        <a href="#" class="text-gray-700 hover:text-orange-600 whitespace-nowrap">Developers</a>
        <a href="#" class="text-gray-700 hover:text-orange-600 whitespace-nowrap">Pricing</a>
        <a href="#" class="text-gray-700 hover:text-orange-600 whitespace-nowrap">Demo</a>
      </nav>

      <!-- Botones derecha -->
      <!-- En md+ visible, en lg ya también Login -->
      <nav class="hidden md:flex items-center space-x-4 ml-auto">
        <!-- Login solo visible lg -->
        <a href="#" class="text-gray-700 hover:text-orange-600 hidden lg:inline-block whitespace-nowrap">Login</a>

        <!-- Contact Sales visible md+ -->
        <a href="#" 
           class="border border-orange-600 text-orange-600 px-4 py-2 rounded hover:bg-orange-50 transition whitespace-nowrap">
          Contact Sales
        </a>

        <!-- Get Started visible md+ -->
        <button
          @click="showModal = true"
          class="ml-4 bg-orange-600 text-white px-4 py-2 rounded whitespace-nowrap"
        >
          Get started
        </button>
      </nav>

      <!-- Botón hamburguesa visible en md y sm a la derecha -->
      <button
        @click="showMenu = !showMenu"
        aria-label="Toggle menu"
        class="ml-4 md:inline-block lg:hidden focus:outline-none"
      >
        <svg class="h-6 w-6 text-gray-700" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16" />
        </svg>
      </button>

    </div>

    <!-- Menú hamburguesa solo para md y sm -->
    <div v-if="showMenu" class="bg-white shadow-md border-t border-gray-200 lg:hidden">
      <nav class="flex flex-col space-y-2 p-4">
        <!-- SOLO botones centrales en menú hamburguesa -->
        <a href="#" class="text-gray-700 hover:text-orange-600">Product</a>
        <a href="#" class="text-gray-700 hover:text-orange-600">Use Cases</a>
        <a href="#" class="text-gray-700 hover:text-orange-600">Developers</a>
        <a href="#" class="text-gray-700 hover:text-orange-600">Pricing</a>
        <a href="#" class="text-gray-700 hover:text-orange-600">Demo</a>
      </nav>
    </div>

  </header>
</template>
<script>
export default {
  data() {
    return {
      showMenu: false,
      showModal: false,
      windowWidth: window.innerWidth,
    };
  },
};
</script>