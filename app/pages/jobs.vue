<script setup lang="ts">
//👉 Imports
import ToolBar from "~/components/jobs/ToolBar.vue";
import ListJobs from "~/components/jobs/ListJobs.vue";
import Container from "~/components/shared/Container.vue";

// ── Shared UInput ui prop ─────────────────────────────────────────────────────
const inputUi = {
  base: "cursor-pointer py-3 ps-12! border-none focus-visible:ring-1 focus-visible:ring-inset focus-visible:ring-[#EBEBEB] rounded-xl text-[#6B7280] placeholder:font-normal placeholder:text-[#6B7280] placeholder:text-[14px] ring-0 focus:ring-0 bg-[#F3F4F3] h-auto",
  leading: "ps-5!",
  leadingIcon: "text-[#94A3B8]! size-5!",
  itemLabel: "rtl:text-end",
};

//👉 Data
const cities = [
  { label: "الرياض", value: "رياض" },
  { label: "جدة", value: "جدة" },
  { label: "مكة", value: "مكة" },
];
const isLoading = ref(false);
</script>

<template>
  <Container>
    <div
      class="jobs-container flex flex-col lg:gap-10 sm:gap-8 gap-5 lg:my-20 sm:my-14 my-10"
    >
      <!-- Toolbar  -->
      <ToolBar :cities="cities" :is-loading="isLoading" :input-ui="inputUi" />
      <!-- Jobs / Filter    -->
      <div class="grid grid-cols-12 sm:gap-6 gap-4">
        <!-- List Jobs -->
        <ListJobs class="lg:col-span-8" />
      </div>
    </div>
  </Container>
</template>
