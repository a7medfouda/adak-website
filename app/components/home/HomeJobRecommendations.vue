<template>
  <section class="py-12 md:py-24">
    <SharedContainer>
      <!-- Header -->
      <div class="flex flex-col md:flex-row md:items-end justify-between gap-6 mb-12">
        <div class="max-w-2xl text-left">
          <h2 class="text-3xl md:text-4xl font-black text-[#002122] mb-2">Recommended Jobs For You</h2>
          <p class="text-base text-[#506262]">Jobs selected specifically for you based on your skills and experience.</p>
        </div>
        <NuxtLink to="/jobs" class="flex items-center gap-2 text-[#0f766e] font-bold hover:text-teal-800 transition-colors self-start md:self-auto">
          <span class="text-sm md:text-base">View All</span>
          <svg width="8" height="12" viewBox="0 0 8 12" fill="none" xmlns="http://www.w3.org/2000/svg" class="w-2 h-3">
            <path d="M1 11L6 6L1 1" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </NuxtLink>
      </div>

      <!-- Jobs Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <SharedJobCard v-for="i in 3" :key="i" />
      </div>
    </SharedContainer>
  </section>
</template>

<script setup lang="ts">
</script>
