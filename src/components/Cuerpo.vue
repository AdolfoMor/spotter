<template>
  <div class="min-h-screen flex items-center justify-center p-6">
    <div class="max-w-6xl w-full grid grid-cols-1 md:grid-cols-3 gap-8">
      <!-- Panel principal -->
      <div class="md:col-span-2 rounded-xl shadow-lg p-10 flex flex-col justify-between">
        <div>
          <span class="text-white text-xs px-2 py-1 rounded">Why Fingerprint</span>
          <h1 class="mt-4 text-4xl font-bold">
            The internet's most <span class="text-orange-500">accurate</span> visitor identifier
          </h1>
          <p class="mt-4 text-gray-700 font-semibold">
            Industry-leading accuracy <span class="font-normal">that lasts for months or years, even when cookies are cleared.</span>
          </p>
        </div>
        <button class="mt-8 w-40 text-white font-semibold py-2 rounded hover:bg-gray-200 transition">
          Learn More
        </button>
        <!-- Aquí puedes poner el gráfico (usa un SVG, imagen o componente de gráfico) -->
        <div class="mt-8">
          <!-- Ejemplo de gráfico simulado -->
           <Tabla />
          <!-- <div class="h-32 bg-gradient-to-r from-orange-300 to-purple-300 rounded"></div> -->
        </div>
      </div>
      <!-- Panel derecho: tarjetas -->
      <div class="flex flex-col gap-6">
        <div class="rounded-xl shadow p-6 flex flex-col gap-2">
          <span class="text-orange-500 text-2xl">🔎</span>
          <h2 class="font-semibold">Any browser, any device.</h2>
          <p class="text-gray-600 text-sm">Identify returning web and mobile app visitors on all browsers, iOS, and Android, with exceptional accuracy.</p>
        </div>
        <div class="rounded-xl shadow p-6 flex flex-col gap-2">
          <span class="text-orange-500 text-2xl">🕵️‍♂️</span>
          <h2 class="font-semibold">Identify all anonymous visitors.</h2>
          <p class="text-gray-600 text-sm">Get details on suspicious visitors even when VPN, incognito mode, or a tampered browser or device is used.</p>
        </div>
        <div class="rounded-xl shadow p-6 flex flex-col gap-2">
          <span class="text-orange-500 text-2xl">🎉</span>
          <h2 class="font-semibold">Delight your trusted users.</h2>
          <p class="text-gray-600 text-sm">Personalize user experience and reduce 2FA and OTP requirements by identifying logged-out users.</p>
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