<template>
  <section class="bg-[#f3f4f3] py-16 md:py-24">
    <SharedContainer>
      <!-- Header -->
      <div class="flex flex-col gap-4 mb-12 md:mb-16 max-w-3xl text-left">
        <h2 class="text-2xl md:text-3xl font-black text-[#002122]">
          Why choose ADAK platform?
        </h2>
        <p class="text-sm md:text-base text-[#506262]">
          We offer an integrated recruitment experience powered by AI to save time and effort and ensure the best results for both companies and job seekers.
        </p>
      </div>

      <!-- Features Grid -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 md:gap-8 lg:gap-12">
        <!-- Feature 1 -->
        <div
          class="bg-white rounded-3xl p-8 md:p-10 flex flex-col items-center text-center border border-slate-100 shadow-sm"
        >
          <div
            class="w-20 h-20 md:w-24 md:h-24 mb-6 md:mb-8 text-[#0D9488] flex items-center justify-center"
          >
            <UIcon name="i-heroicons-bolt" class="w-full h-full" />
          </div>
          <h3 class="text-lg md:text-xl font-black text-[#1a1c1c] mb-4">
            Speed in Recruitment
          </h3>
          <p class="text-sm md:text-base text-[#506262] leading-relaxed">
            Reach the best candidates in record time with smart matching technologies.
          </p>
        </div>

        <!-- Feature 2 -->
        <div
          class="bg-white rounded-3xl p-8 md:p-10 flex flex-col items-center text-center border border-slate-100 shadow-sm"
        >
          <div
            class="w-20 h-20 md:w-24 md:h-24 mb-6 md:mb-8 text-[#0D9488] flex items-center justify-center"
          >
            <UIcon name="i-heroicons-shield-check" class="w-full h-full" />
          </div>
          <h3 class="text-lg md:text-xl font-black text-[#1a1c1c] mb-4">
            High Reliability
          </h3>
          <p class="text-sm md:text-base text-[#506262] leading-relaxed">
            Verified companies and verified candidates to ensure a safe recruitment environment.
          </p>
        </div>

        <!-- Feature 3 -->
        <div
          class="bg-white rounded-3xl p-8 md:p-10 flex flex-col items-center text-center border border-slate-100 shadow-sm"
        >
          <div
            class="w-20 h-20 md:w-24 md:h-24 mb-6 md:mb-8 flex items-center justify-center"
          >
            <img
              src="/imgs/feature-icon.svg"
              alt="Feature Icon"
              class="w-full h-full object-contain"
            />
          </div>
          <h3 class="text-lg md:text-xl font-black text-[#1a1c1c] mb-4">
            Advanced Analytics
          </h3>
          <p class="text-sm md:text-base text-[#506262] leading-relaxed">
            Comprehensive reports on market trends and candidate performance to support your decisions.
          </p>
        </div>
      </div>
    </SharedContainer>
  </section>
</template>

<script setup lang="ts"></script>
