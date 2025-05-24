<template>

    <header class="shadow-sm sticky top-0 z-10">
    <div class="max-w-7xl mx-auto px-4 py-3 flex items-center justify-between relative text-sm">

      <!-- Logo a la izquierda -->
      <div class="flex items-center space-x-2 text-lg font-bold text-white">
        <svg width="80" height="80" viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg">
          <rect x="10" y="20" width="60" height="40" rx="4"/>
          <circle cx="24" cy="32" r="8" fill="#F85D6C"/>
          <circle cx="24" cy="48" r="8" fill="#179393"/>
          <circle cx="40" cy="48" r="8" fill="#B0D3D6"/>
          <circle cx="56" cy="48" r="8" fill="#B0D3D6"/>
        </svg>
        <span>Spotter</span>
      </div>




      <!-- Botones centrales centrados absolutamente solo en lg -->
      <nav
        class="hidden lg:flex space-x-6 absolute left-1/2 top-1/2 transform -translate-x-1/2 -translate-y-1/2"
      >
        <a href="#" class="text-white hover:text-[#176B74] whitespace-nowrap">Product</a>
        <a href="#" class="text-white hover:text-[#176B74] whitespace-nowrap">Use Cases</a>
        <a href="#" class="text-white hover:text-[#176B74] whitespace-nowrap">Developers</a>
        <a href="#" class="text-white hover:text-[#176B74] whitespace-nowrap">Pricing</a>
        <a href="#" class="text-white hover:text-[#176B74] whitespace-nowrap">Demo</a>
      </nav>

      <!-- Botones derecha -->
      <!-- md+ -->
      <nav class="hidden md:flex items-center space-x-4 ml-auto">
        <!-- Login solo visible lg -->
        <a href="#" class="text-white hover:text-[#176B74] hidden lg:inline-block whitespace-nowrap">Login</a>

        <!-- md+ -->
        <a href="#" 
           class="border px-4 py-2 rounded whitespace-nowrap transition
          border-[#176B74] text-[#176B74] 
          hover:bg-[#176B74]/20 hover:text-[#124E5B]">
          Contact Sales
        </a>

        <!--  md+ -->
        <button
          @click="showModal = true"
          class="ml-4 px-4 py-2 rounded whitespace-nowrap
         bg-[#176B74] text-white
         hover:bg-[#124E5B] transition"
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
        <a href="#" class="text-gray-700 hover:text-[#176B74]">Product</a>
        <a href="#" class="text-gray-700 hover:text-[#176B74]">Use Cases</a>
        <a href="#" class="text-gray-700 hover:text-[#176B74]">Developers</a>
        <a href="#" class="text-gray-700 hover:text-[#176B74]">Pricing</a>
        <a href="#" class="text-gray-700 hover:text-[#176B74]">Demo</a>
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