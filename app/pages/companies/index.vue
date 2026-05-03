<template>
  <div class="min-h-screen bg-[#f9fafa] pt-32 pb-24">
    <SharedContainer>
      <!-- Search Section -->
      <div class="bg-white rounded-[24px] p-4 shadow-sm mb-12 w-full mx-auto">
        <div class="flex flex-col md:flex-row gap-4 w-full items-center justify-between">
          
          <div class="flex flex-col md:flex-row gap-4 w-full md:w-auto flex-1">
             <!-- Location Input -->
             <div class="flex-1 md:max-w-xs">
              <UInput
                v-model="locationQuery"
                icon="i-heroicons-map-pin"
                placeholder="City"
                :ui="inputUi"
                class="w-full"
              />
            </div>
            
            <!-- Search Input -->
            <div class="flex-1">
              <UInput
                v-model="searchQuery"
                icon="i-heroicons-magnifying-glass"
                placeholder="Search for a company"
                :ui="inputUi"
                class="w-full"
              />
            </div>
          </div>

          <!-- Search Button -->
          <button
            class="bg-[#147b71] hover:bg-[#0f625a] text-white px-8 py-3 w-full md:w-auto rounded-[32px] font-bold text-sm transition-colors flex items-center justify-center gap-2"
          >
            <UIcon name="i-heroicons-arrow-left" class="w-4 h-4 rtl:rotate-180" />
            Search
          </button>
        </div>
      </div>

      <!-- Section Title -->
      <div class="flex flex-col md:flex-row md:items-end justify-between gap-4 mb-8">
        <div>
          <h2 class="text-2xl sm:text-3xl font-black text-[#002122] mb-2">
            All Companies
          </h2>
          <p class="text-[#506262] text-sm">
            Explore more than 200 partner companies
          </p>
        </div>
      </div>

      <!-- Companies Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <NuxtLink
          v-for="company in companies"
          :key="company.id"
          :to="`/companies/${company.id}`"
          class="bg-white rounded-[16px] p-6 flex flex-col gap-4 border border-transparent hover:border-gray-100 transition-all hover:shadow-md group"
        >
          <!-- Top Row: Logo and Badge -->
          <div class="flex items-start justify-between">
            <div class="w-16 h-16 rounded-[12px] overflow-hidden shrink-0" :style="{ backgroundColor: company.logoBg }">
              <img
                :src="company.logo"
                :alt="company.name"
                class="w-full h-full object-cover mix-blend-multiply opacity-90 p-2"
              />
            </div>
            <div
              class="bg-[#4c2814] text-[#c38d73] px-3 py-1 rounded-full text-xs font-bold shrink-0 mt-1"
            >
              {{ company.openJobs }} Open Jobs
            </div>
          </div>

          <!-- Middle: Content -->
          <div class="flex flex-col gap-2 mt-2 flex-1">
            <h3 class="text-xl font-bold text-[#1a1c1c] leading-tight">
              {{ company.name }}
            </h3>
            <p class="text-sm text-[#404848] leading-relaxed line-clamp-2 min-h-[44px]">
              {{ company.description }}
            </p>
          </div>

          <!-- Bottom: Action -->
          <div class="border-t border-gray-100 pt-4 mt-2">
            <button
              class="w-full bg-[#00383a] group-hover:bg-[#002122] text-white px-5 py-2.5 rounded-lg text-sm font-bold transition-colors"
            >
              View Jobs
            </button>
          </div>
        </NuxtLink>
      </div>
    </SharedContainer>
  </div>
</template>

<script setup lang="ts">
const searchQuery = ref('');
const locationQuery = ref('');

const inputUi = {
  base: "px-4 py-3 border border-[#EBEBEB] focus-visible:ring-1 focus-visible:ring-inset focus-visible:ring-[#EBEBEB] rounded-[32px] text-gray-900 placeholder:text-gray-500 placeholder:text-[14px] font-normal ring-0 focus:ring-0 bg-[#f9fafa]",
  icon: {
    base: "text-gray-500",
  }
};

const companies = [
  {
    id: 1,
    name: "Advanced Tech Company",
    description: "Leading company in AI solutions and cloud software development in the Arab region.",
    logo: "https://ui-avatars.com/api/?name=AT&background=fff&color=00383a&size=128",
    logoBg: "#bbebed",
    openJobs: 15,
  },
  {
    id: 2,
    name: "Modern Building Group",
    description: "We design the future through sustainable architectural projects and innovative engineering solutions.",
    logo: "https://ui-avatars.com/api/?name=MB&background=fff&color=00383a&size=128",
    logoBg: "#223b3c",
    openJobs: 8,
  },
  {
    id: 3,
    name: "Knowledge Academy",
    description: "An educational platform aiming to empower Arab youth with the technical skills needed for the job market.",
    logo: "https://ui-avatars.com/api/?name=KA&background=fff&color=00383a&size=128",
    logoBg: "#0f5a63",
    openJobs: 3,
  },
  {
    id: 4,
    name: "Digital Horizon Agency",
    description: "Your strategic partner for digital growth, specializing in brand building and social media campaigns.",
    logo: "https://ui-avatars.com/api/?name=DH&background=fff&color=00383a&size=128",
    logoBg: "#161622",
    openJobs: 22,
  },
  {
    id: 5,
    name: "Smart Solutions Inc.",
    description: "Providing smart IoT solutions and data analytics for enterprises and startups.",
    logo: "https://ui-avatars.com/api/?name=SS&background=fff&color=00383a&size=128",
    logoBg: "#0f766e",
    openJobs: 12,
  },
  {
    id: 6,
    name: "Green Energy Corp",
    description: "Pioneering renewable energy projects and sustainable resource management.",
    logo: "https://ui-avatars.com/api/?name=GE&background=fff&color=00383a&size=128",
    logoBg: "#4d7c0f",
    openJobs: 5,
  }
];
</script>
