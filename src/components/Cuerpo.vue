<template>
  <div class="container mx-auto px-4 py-8 max-w-3xl">
    <!-- Sección principal  -->
    <div class="border border-gray-300 p-6 mb-8 text-center rounded-lg">
      <div class="space-y-4"> <!-- Div para el título y texto -->
        <h1 class="text-3xl font-bold">The internet's most accurate visitor identifier</h1>
        <p class="text-xl"><strong>Industry-leading accuracy</strong> that lasts for months or years...</p>
      </div>
      
      <!-- Contenedor del gráfico  -->
      <div class="border-2 border-dashed border-gray-400 h-48 my-8 rounded-lg"></div>
      
      <!-- Leyenda del gráfico -->
      <div class="flex justify-between text-sm text-gray-600 mb-1 px-2">
        <span>0</span><span>30</span><span>60</span><span>90</span><span>120</span>
      </div>
      <p class="text-xs uppercase tracking-wider text-gray-500">ACCURACY DROPOFF DAYS AFTER INITIAL IDENTIFICATION</p>
      
      <!-- Botón  -->
      <div class="mt-8">
        <div class="inline-block border border-gray-400 px-6 py-2 rounded-md">Learn More</div>
      </div>
    </div>

    <!-- Secciones de características (3 cajas) -->
    <div class="grid md:grid-cols-2 gap-6">
      <!-- Caja 1 -->
      <div class="border-l-4 border-gray-400 p-5 bg-gray-50 rounded-r-lg">
        <h3 class="text-xl font-semibold mb-3">Any browser, any device.</h3>
        <div class="h-16 border border-gray-300 rounded"></div> <!-- Texto placeholder -->
      </div>
      
      <!-- Caja 2 -->
      <div class="border-l-4 border-gray-400 p-5 bg-gray-50 rounded-r-lg">
        <h3 class="text-xl font-semibold mb-3">Identify all anonymous visitors.</h3>
        <div class="h-16 border border-gray-300 rounded"></div> <!-- Texto placeholder -->
      </div>
      
      <!-- Caja 3 (full width en móvil, 2 cols en desktop) -->
      <div class="border-l-4 border-gray-400 p-5 bg-gray-50 rounded-r-lg md:col-span-2">
        <h3 class="text-xl font-semibold mb-3">Delight your trusted users.</h3>
        <div class="h-16 border border-gray-300 rounded"></div> <!-- Texto placeholder -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'StructureOnly'
}
</script>