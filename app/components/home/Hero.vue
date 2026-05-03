<script setup lang="ts">
// Hero section for the home page
</script>

<template>
  <div class="relative w-full bg-[#00383A] pt-12 pb-48 md:pt-20 md:pb-40 lg:pb-48 overflow-visible overflow-x-clip">
    <!-- Background SVG (contains background color, blobs, and pattern) -->
    <div class="absolute inset-0 z-0 pointer-events-none overflow-hidden">
      <img src="/imgs/hero-bg.svg" class="w-full h-full object-cover object-top" alt="" />
    </div>

    <SharedContainer class="relative z-10 h-full flex flex-col justify-center">
      <div class="flex flex-col lg:flex-row items-center justify-between gap-12 lg:gap-8">
        
        <!-- Left Column: Feature Boxes (Becomes Top/Middle on mobile) -->
        <div class="flex flex-col gap-4 md:gap-6 relative justify-center items-start w-full lg:w-1/3 order-3 lg:order-1 mt-8 lg:mt-0">
          
          <!-- Feature 1: Ai CV Screening -->
          <div class="flex items-center gap-3 md:gap-4 px-4 md:px-6 py-3 md:py-4 rounded-[12px] md:rounded-[16px] border border-[rgba(1,130,127,0.60)] bg-[rgba(255,255,255,0.04)] backdrop-blur-md w-full max-w-[320px] relative z-10 lg:ml-auto transform hover:scale-[1.02] transition-transform shadow-lg shadow-black/20 self-start lg:self-auto ltr:flex-row rtl:flex-row-reverse">
            <div class="flex-1 ltr:text-left rtl:text-right">
              <div class="text-xs md:text-sm text-[#2DD4BF] font-sans font-medium mb-0.5" dir="ltr">AI CV Screening</div>
              <div class="text-white text-sm md:text-base font-medium">Smart resume analysis</div>
            </div>
            <img src="/icons/cv-screening-icon.svg" class="w-10 h-10 md:w-12 md:h-12 object-contain shrink-0" alt="Icon" />
          </div>

          <!-- Feature 2: Ai Matching -->
          <div class="flex items-center gap-3 md:gap-4 px-4 md:px-6 py-3 md:py-4 rounded-[12px] md:rounded-[16px] border border-[rgba(1,130,127,0.60)] bg-[rgba(255,255,255,0.04)] backdrop-blur-md w-full max-w-[320px] relative z-10 lg:ml-auto transform lg:-translate-x-4 hover:scale-[1.02] transition-transform shadow-lg shadow-black/20 self-center lg:self-auto ltr:flex-row rtl:flex-row-reverse">
            <div class="flex-1 ltr:text-left rtl:text-right">
              <div class="text-xs md:text-sm text-[#2DD4BF] font-sans font-medium mb-0.5" dir="ltr">AI Matching</div>
              <div class="text-white text-sm md:text-base font-medium">Smart candidate matching</div>
            </div>
            <img src="/icons/matching-icon.svg" class="w-10 h-10 md:w-12 md:h-12 object-contain shrink-0" alt="Icon" />
          </div>

          <!-- Feature 3: Ai Persona Analysis -->
          <div class="flex items-center gap-3 md:gap-4 px-4 md:px-6 py-3 md:py-4 rounded-[12px] md:rounded-[16px] border border-[rgba(1,130,127,0.60)] bg-[rgba(255,255,255,0.04)] backdrop-blur-md w-full max-w-[320px] relative z-10 lg:ml-auto transform hover:scale-[1.02] transition-transform shadow-lg shadow-black/20 self-end lg:self-auto ltr:flex-row rtl:flex-row-reverse">
            <div class="flex-1 ltr:text-left rtl:text-right">
              <div class="text-xs md:text-sm text-[#2DD4BF] font-sans font-medium mb-0.5" dir="ltr">AI Persona Analysis</div>
              <div class="text-white text-sm md:text-base font-medium">Personality & fit analysis</div>
            </div>
            <img src="/icons/analysis-icon.svg" class="w-10 h-10 md:w-12 md:h-12 object-contain shrink-0" alt="Icon" />
          </div>
        </div>

        <!-- Center Column: Text & CTAs (Becomes Top on mobile) -->
        <div class="flex flex-col items-center text-center w-full lg:w-1/3 order-1 lg:order-2 z-10">
          <h1 class="text-4xl sm:text-5xl md:text-6xl font-black leading-[1.2] md:leading-[1.3] mb-4 md:mb-6 text-white drop-shadow-md whitespace-pre-line font-['Cairo']">
            Smart <span class="text-[#00b9b9]">Recruitment</span>
            Starts Here
          </h1>
          <p class="text-[rgba(240,253,250,0.9)] text-base sm:text-lg md:text-xl mb-8 md:mb-10 max-w-[672px] leading-relaxed px-4 md:px-0 font-medium">
            An AI-powered recruitment platform connecting top talent with leading companies intelligently and transparently.
          </p>
          <div class="flex flex-col sm:flex-row items-center gap-4 w-full px-4 md:px-0 justify-center">
            <UButton size="xl" class="bg-[#198078] hover:bg-[#156e66] text-white rounded-[12px] px-6 md:px-8 h-12 md:h-14 text-base md:text-lg font-bold w-full sm:w-auto flex justify-center transition-all">
              Start Now for Free
            </UButton>
            <UButton size="xl" variant="outline" class="border-[#FFF] text-white hover:bg-white/10 rounded-[12px] px-6 md:px-8 h-12 md:h-14 text-base md:text-lg font-bold w-full sm:w-auto flex justify-center transition-all">
              Book a Demo
            </UButton>
          </div>
        </div>

        <!-- Right Column: Brain & Shortlisting (Becomes Bottom on mobile) -->
        <div class="flex flex-col items-center justify-center w-full lg:w-1/3 order-2 lg:order-3 z-10 relative mt-8 lg:mt-0 lg:ml-8">
          <img src="/imgs/ai.png" alt="AI Brain" class="w-48 sm:w-64 max-w-full lg:max-w-[320px] drop-shadow-[0_0_30px_rgba(45,212,191,0.2)] mb-4 md:mb-8 animate-pulse-slow" />
          
          <div class="flex items-center gap-3 md:gap-4 px-4 md:px-6 py-3 md:py-4 rounded-[12px] md:rounded-[16px] border border-[rgba(1,130,127,0.60)] bg-[rgba(255,255,255,0.04)] backdrop-blur-md w-full max-w-[320px] ltr:flex-row rtl:flex-row-reverse transform hover:scale-[1.02] transition-transform shadow-lg shadow-black/20 absolute bottom-0 lg:-bottom-12 right-0 lg:-right-12">
            <div class="flex-1 ltr:text-left rtl:text-right">
              <div class="text-xs md:text-sm text-[#2DD4BF] font-sans font-medium mb-0.5" dir="ltr">Shortlisting</div>
              <div class="text-white text-sm md:text-base font-medium">Top candidate nomination</div>
            </div>
            <img src="/icons/recommendation-icon.svg" class="w-10 h-10 md:w-12 md:h-12 object-contain shrink-0" alt="Icon" />
          </div>
        </div>

      </div>
    </SharedContainer>

    <!-- Floating Search Section -->
    <div class="absolute -bottom-40 md:-bottom-24 lg:-bottom-16 left-1/2 -translate-x-1/2 w-[calc(100%-2rem)] md:w-full px-0 md:px-4 z-20" style="max-width: 1024px;">
      <div class="bg-white rounded-[16px] md:rounded-2xl shadow-[0_10px_40px_rgba(0,0,0,0.1)] p-4 md:p-6 lg:p-8 relative">
        
        <div class="flex flex-col md:flex-row items-center gap-3 md:gap-4 mb-4 md:mb-6 w-full">
          <!-- Search input container -->
          <div class="flex-1 w-full relative">
            <UInput 
              icon="i-heroicons-magnifying-glass" 
              size="xl" 
              placeholder="Job title or keywords" 
              :ui="{ base: 'bg-[#F3F4F3] border-none rounded-[12px] h-12 md:h-14 px-3 md:px-4 text-sm md:text-base text-gray-700 w-full', icon: { base: 'text-gray-400' } }" 
            />
          </div>

          <!-- Divider for desktop only -->
          <div class="hidden md:block w-px h-8 bg-gray-200"></div>

          <!-- Location Input -->
          <div class="w-full md:w-[240px] relative">
            <UInput 
              icon="i-heroicons-map-pin" 
              size="xl" 
              placeholder="City" 
              :ui="{ base: 'bg-[#F3F4F3] border-none rounded-[12px] h-12 md:h-14 px-3 md:px-4 text-sm md:text-base text-gray-700 w-full', icon: { base: 'text-gray-400' } }" 
            />
          </div>

          <!-- Search Button -->
          <UButton 
            size="xl" 
            class="bg-[#198078] hover:bg-[#156e66] text-white rounded-[12px] h-12 md:h-14 px-6 md:px-8 w-full md:w-auto flex items-center justify-center gap-2 font-bold text-base transition-colors"
          >
            Search
          </UButton>
        </div>

        <!-- Quick Filters -->
        <div class="flex flex-wrap items-center gap-2 md:gap-3">
          <span class="text-xs md:text-sm text-gray-500 font-medium whitespace-nowrap ltr:pr-2 rtl:pl-2">Quick Filter:</span>
          <button class="px-4 py-1.5 md:py-2 rounded-full bg-[#D1E3E4] text-[#198078] text-xs md:text-sm font-semibold hover:bg-[#c2d7d8] transition-colors">
            Latest Jobs
          </button>
          <button class="px-4 py-1.5 md:py-2 rounded-full bg-[#E2E3E2] text-gray-600 hover:bg-gray-300 text-xs md:text-sm font-medium transition-colors">
            Remote
          </button>
          <button class="px-4 py-1.5 md:py-2 rounded-full bg-[#E2E3E2] text-gray-600 hover:bg-gray-300 text-xs md:text-sm font-medium transition-colors">
            Full Time
          </button>
          <button class="px-4 py-1.5 md:py-2 rounded-full bg-[#E2E3E2] text-gray-600 hover:bg-gray-300 text-xs md:text-sm font-medium transition-colors">
            IT
          </button>
        </div>

      </div>
    </div>
  </div>
</template>

<style scoped>
.animate-pulse-slow {
  animation: pulse 4s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}
@keyframes pulse {
  0%, 100% { opacity: 1; transform: scale(1); }
  50% { opacity: 0.9; transform: scale(0.98); }
}
</style>
