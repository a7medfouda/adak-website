<template>
  <SharedContainer class="pb-24">
    <div class="bg-[#00383a] rounded-4xl overflow-hidden relative shadow-2xl">
      <!-- Background overlay effect -->
      <div
        class="absolute inset-0 opacity-10 pointer-events-none mix-blend-overlay bg-linear-to-tr from-white/0 via-white/20 to-white/0"
      />

      <div
        class="grid grid-cols-1 lg:grid-cols-2 gap-12 p-8 sm:p-12 lg:p-16 relative z-10"
      >
        <!-- Text Content -->
        <div class="flex flex-col gap-8 justify-center order-2 lg:order-1">
          <h2 class="text-3xl sm:text-4xl font-black text-white leading-tight">
            Are you looking for the best talent for your company?
          </h2>

          <p
            class="text-[#a0cfd1] text-base sm:text-lg leading-relaxed max-w-lg"
          >
            Join thousands of companies using 'Adak' to access exceptional competencies and manage recruitment processes with high efficiency.
          </p>

          <div class="flex flex-col sm:flex-row gap-4 mt-2">
            <button
              class="cursor-pointer bg-[#d4e6e6] text-[#0e1e1f] px-8 py-2.5 rounded-xl font-bold text-sm sm:text-base hover:bg-white transition-colors text-center"
            >
              Register your company now
            </button>
            <button
              class="cursor-pointer border border-white/20 text-white px-8 py-2.5 rounded-xl font-bold text-sm sm:text-base hover:bg-white/10 transition-colors text-center"
            >
              Contact Sales Team
            </button>
          </div>
        </div>

        <!-- Image -->
        <div
          class="flex items-center justify-center lg:justify-end order-1 lg:order-2"
        >
          <div
            class="relative w-full max-w-[450px] aspect-square rounded-[1.5rem] overflow-hidden shadow-2xl"
          >
            <img
              src="https://images.unsplash.com/photo-1560250097-0b93528c311a?w=1000&q=80"
              alt="Business Strategy"
              class="absolute inset-0 w-full h-full object-cover object-top"
            />
          </div>
        </div>
      </div>
    </div>
  </SharedContainer>
</template>

<script setup>
const { t } = useI18n();
</script>
