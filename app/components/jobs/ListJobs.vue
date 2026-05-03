<script setup lang="ts">
//👉 Imports
import JobGrowth from "../icons/JobGrowth.vue";
import JobCard from "./JobCard.vue";
</script>

<template>
  <div class="list-jobs-container sm:space-y-6 space-y-4">
    <!-- Statistics  -->
    <div class="jobs_statistics-container grid grid-cols-12 gap-4">
      <!-- Number of jobs  -->
      <div
        class="jobs_numbers-container lg:col-span-8 sm:col-span-7 col-span-12"
      >
        <h3 class="lg:text-xl sm:text-lg text-base text-white">
          اكتشف 1,240 وظيفة متاحة اليوم
        </h3>
        <p class="text-[#BBEBED]">
          وظائف مخصصة لمهاراتك في البرمجة والتصميم وتطوير الأعمال.
        </p>
      </div>
      <!-- Overview  -->
      <div
        class="jobs_statistics_overview-container lg:col-span-4 sm:col-span-5 col-span-12"
      >
        <p class="font-bold">نظرة عامة على الوظائف</p>
        <div class="flex items-center gap-2">
          <h2 class="lg:text-3xl sm:text-2xl text-xl font-bold text-[#002122]">
            نمو 12%
          </h2>
          <JobGrowth class="shrink-0" />
        </div>
        <p class="text-xs">زيادة في طلب المطورين هذا الشهر</p>
      </div>
    </div>
    <!-- List  -->
    <JobCard v-for="i in 6" :key="i" />
  </div>
</template>
<style lang="scss">
.list-jobs-container {
  .jobs_statistics-container {
    .jobs_numbers-container {
      border-radius: 16px;
      background: linear-gradient(135deg, #00383a 0%, #004a4d 100%);
      box-shadow:
        0 10px 30px -5px rgba(0, 0, 0, 0.04),
        0 4px 12px -2px rgba(0, 0, 0, 0.03);
      padding: 16px;
      display: flex;
      flex-direction: column;
      gap: 8px;
    }
    .jobs_statistics_overview-container {
      border-radius: 16px;
      background: #d1e3e4;
      box-shadow:
        0 10px 30px -5px rgba(0, 0, 0, 0.04),
        0 4px 12px -2px rgba(0, 0, 0, 0.03);
      padding: 16px;
      display: flex;
      flex-direction: column;
      gap: 4px;
    }
  }
  @media (min-width: 640px) {
    .jobs_statistics-container {
      .jobs_numbers-container,
      .jobs_statistics_overview-container {
        padding: 28px;
      }
    }
  }
}
</style>
