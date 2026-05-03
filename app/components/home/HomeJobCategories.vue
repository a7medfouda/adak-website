<template>
  <section class="pt-12 md:pt-24">
    <SharedContainer>
      <!-- Header -->
      <div class="flex flex-col md:flex-row md:items-end justify-between gap-6 mb-12">
        <div class="max-w-2xl text-left">
          <h2 class="text-3xl md:text-4xl font-black text-[#002122] mb-2">Explore jobs by category</h2>
          <p class="text-base text-[#506262]">Thousands of opportunities await you in various vital sectors, choose your career path today.</p>
        </div>
        <NuxtLink to="/categories" class="flex items-center gap-2 text-[#0f766e] font-bold hover:text-teal-800 transition-colors self-start md:self-auto">
          <span class="text-sm md:text-base">View All</span>
          <svg width="8" height="12" viewBox="0 0 8 12" fill="none" xmlns="http://www.w3.org/2000/svg" class="w-2 h-3">
            <path d="M1 11L6 6L1 1" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </NuxtLink>
      </div>

      <!-- Categories Grid -->
      <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-4 md:gap-6">
        <NuxtLink 
          v-for="i in 6" 
          :key="i"
          to="/categories/programming"
          class="bg-white rounded-2xl p-6 md:p-8 flex flex-col items-center text-center group"
        >
          <!-- Icon Circle -->
          <div class="w-20 h-20 md:w-24 md:h-24 rounded-full bg-[#f0fdfa] flex items-center justify-center mb-6">
            <img src="/imgs/job-icon.svg" alt="Category Icon" class="w-10 h-10 md:w-14 md:h-14" />
          </div>
          
          <!-- Category Details -->
          <h3 class="text-sm sm:text-base font-black text-[#1a1c1c] mb-2">Programming & Tech</h3>
          <p class="text-xs text-[#506262]">420 Open Jobs</p>
        </NuxtLink>
      </div>
    </SharedContainer>
  </section>
</template>

<script setup lang="ts">
</script>
