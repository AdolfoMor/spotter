<template>
  <div
    class="fixed bottom-6 right-6 z-50 flex flex-col items-center cursor-pointer select-none"
  >
    <!-- Popover personalizado: aparece justo arriba del botón -->
    <transition name="fade">
      <div
        v-if="showPopover"
        ref="popoverRef"
        class="w-64 p-4 mb-2 bg-white rounded-lg shadow-lg text-left relative"
        @click.stop
      >
        <p class="text-lg font-semibold mb-1">👋 Hi there! Need help?</p>
        <p class="text-gray-700 mb-3 text-sm">Get help with using Spotter.</p>
        <ul class="space-y-2 text-blue-600 font-medium text-sm">
          <li><a href="#" class="hover:underline">Read documentation</a></li>
          <li><a href="#" class="hover:underline">Talk to sales</a></li>
          <li><a href="#" class="hover:underline">Contact support</a></li>
        </ul>
        <button
          @click="joinDiscord"
          class="mt-3 w-full bg-[#7289DA] text-white py-2 rounded hover:bg-[#5b6eae] transition"
        >
          Join Discord
        </button>
      </div>
    </transition>

    <!-- Botón circular -->
    <div
      ref="buttonRef"
      @mouseenter="handleMouseEnter"
      @mouseleave="handleMouseLeave"
      @click="togglePopover"
      class="w-16 h-16 rounded-full shadow-md border border-gray-300 bg-white flex items-center justify-center transition-colors duration-300 relative"
      title="Help & Support"
    >
      <svg
        width="40"
        height="40"
        viewBox="0 0 80 80"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <rect x="10" y="20" width="60" height="40" rx="4" />
        <circle cx="24" cy="32" r="8" :fill="circleColors[0]" />
        <circle cx="24" cy="48" r="8" :fill="circleColors[1]" />
        <circle cx="40" cy="48" r="8" :fill="circleColors[2]" />
        <circle cx="56" cy="48" r="8" :fill="circleColors[3]" />
      </svg>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      originalColors: ['#F85D6C', '#179393', '#B0D3D6', '#B0D3D6'],
      circleColors: ['#F85D6C', '#179393', '#B0D3D6', '#B0D3D6'],
      colors: ['#F85D6C', '#179393', '#B0D3D6'],
      hoverInterval: null,
      showPopover: false,
    };
  },
  methods: {
    handleMouseEnter() {
      if (this.hoverInterval) clearInterval(this.hoverInterval);
      this.hoverInterval = setInterval(() => {
        this.circleColors = this.circleColors.map(() => {
          const idx = Math.floor(Math.random() * this.colors.length);
          return this.colors[idx];
        });
      }, 400);
    },
    handleMouseLeave() {
      clearInterval(this.hoverInterval);
      this.circleColors = [...this.originalColors];
    },
    togglePopover() {
      this.showPopover = !this.showPopover;
    },
    joinDiscord() {
      alert('¡Únete a nuestro Discord!');
    },
    onClickOutside(event) {
      if (
        this.showPopover &&
        this.$refs.popoverRef &&
        !this.$refs.popoverRef.contains(event.target) &&
        !this.$refs.buttonRef.contains(event.target)
      ) {
        this.showPopover = false;
      }
    },
  },
  mounted() {
    document.addEventListener('click', this.onClickOutside);
  },
  beforeUnmount() {
    clearInterval(this.hoverInterval);
    document.removeEventListener('click', this.onClickOutside);
  },
};
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.2s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
