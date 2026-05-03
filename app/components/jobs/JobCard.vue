<script setup lang="ts">
import JobCompany from "../icons/JobCompany.vue";
</script>

<template>
  <div class="job-card-container">
    <div class="job-card_header flex items-center justify-between gap-3">
      <div class="job-card_info">
        <!-- Image  -->
        <div
          class="job-card_image sm:size-14 size-10 overflow-hidden rounded-lg shrink-0"
        >
          <img
            src="/imgs/job.jpg"
            width="56"
            height="56"
            class="w-full h-full object-cover"
          />
        </div>
        <!-- Name / company  -->
        <div class="job-card_details space-y-1">
          <p class="lg:text-lg sm:text-base text-sm font-bold text-[#002122]">
            مطور واجهات أمامية (Senior)
          </p>
          <div class="flex items-center gap-1">
            <JobCompany class="shrink-0" />
            <p>شركة نسيج للحلول الرقمية</p>
          </div>
        </div>
      </div>
      <UButton block class="bg-[#00383A] rounded-2xl py-4 sm:px-9 px-5 font-bold w-fit cursor-pointer">
        قدم الآن</UButton
      >
    </div>
  </div>
</template>
<style lang="scss">
.job-card-container {
  border-radius: 16px;
  background: #fefefe;
  box-shadow:
    0 10px 30px -5px rgba(0, 0, 0, 0.04),
    0 4px 12px -2px rgba(0, 0, 0, 0.03);
  display: flex;
  flex-direction: column;
  gap: 14px;
  padding: 16px;
  .job-card_header {
    .job-card_info {
      display: flex;
      align-items: center;
      gap: 16px;
    }
  }
  @media (min-width: 640px) {
    padding: 24px;
    gap: 20px;
  }
}
</style>
