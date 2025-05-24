<template>
  <div class="min-h-screen flex items-center justify-center p-6 bg-transparent">
    <div class="max-w-6xl w-full grid grid-cols-1 md:grid-cols-3 gap-8 items-stretch">
    <!-- Panel principal -->
    <div class="md:col-span-2 rounded-xl shadow-lg flex flex-col justify-between overflow-hidden">
      <!-- Sección con fondo oscuro -->
      <div class="bg-[#0E3C41] p-10 text-left">
        <span class="text-xs px-2 py-1 rounded bg-[#176B74] inline-block">Why Spotter</span>
        <h1 class="mt-4 text-4xl font-bold">
          The internet's most <span class="text-[#25B5C0]">accurate</span> visitor identifier
        </h1>
        <p class="mt-4 font-semibold">
          Industry-leading accuracy <span class="font-normal">that lasts for months or years, even when cookies are cleared.</span>
        </p>
        <button class="mt-8 w-40 text-white font-semibold py-2 rounded hover:bg-[#176B74] transition bg-[#124C52]">
          Learn More
        </button>
      </div>

      <!-- Sección con fondo claro -->
      <div class="bg-white p-6 text-black">
        <Tabla />
      </div>
    </div>



      <!-- Panel derecho: tarjetas -->
      <div class="flex flex-col gap-6 h-full">
        <div class="flex-1 rounded-xl shadow p-6 flex flex-col justify-start text-left bg-[#124C52] text-white">
          <div class="flex items-center gap-2 mb-2">
            <span class="text-2xl">🔎</span>
            <h2 class="font-semibold text-lg">Ready now</h2>
          </div>
          <p class="text-gray-300 text-sm">
            Set the times when you will be ready.
          </p>
        </div>

        <div class="flex-1 rounded-xl shadow p-6 flex flex-col justify-start text-left bg-[#124C52] text-white">
          <div class="flex items-center gap-2 mb-2">
            <span class="text-2xl">🕵️‍♂️</span>
            <h2 class="font-semibold text-lg">Select destinations</h2>
          </div>
          <p class="text-gray-300 text-sm">
            Select the markets you want to go to, avoid bad markets via NO-GO map.
          </p>
        </div>

        <div class="flex-1 rounded-xl shadow p-6 flex flex-col justify-start text-left bg-[#124C52] text-white">
          <div class="flex items-center gap-2 mb-2">
            <span class="text-2xl">🎉</span>
            <h2 class="font-semibold text-lg">Spotter recommends loads</h2>
          </div>
          <p class="text-gray-300 text-sm">
            Get matched with the highest load score offers
          </p>
        </div>
      </div>
    </div>
  </div>
</template>




<script>
import Tabla from './Tabla.vue';
export default {
components: 
  {  
    Tabla
  },
  name: 'StructureOnly'
}
</script>