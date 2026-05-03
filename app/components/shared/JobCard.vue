<template>
  <div
    class="bg-white rounded-2xl p-6 flex flex-col gap-5 relative"
    style="
      box-shadow:
        0px 10px 30px -5px rgba(0, 0, 0, 0.04),
        0px 4px 12px -2px rgba(0, 0, 0, 0.03);
    "
  >
    <!-- Company & Title -->
    <div class="flex items-start gap-4">
      <!-- Logo -->
      <div
        class="w-14 h-14 rounded-xl bg-gray-100 flex items-center justify-center shrink-0 overflow-hidden border border-gray-50"
      >
        <img
          src="https://ui-avatars.com/api/?name=Naseej&background=0f766e&color=fff&size=128"
          alt="Company Logo"
          class="w-full h-full object-cover"
        />
      </div>
      <!-- Text Content -->
      <div class="flex flex-col gap-1.5 flex-1 pt-1">
        <h3 class="font-bold text-[#1a1c1c] text-lg leading-tight">
          Senior Frontend Developer
        </h3>
        <div class="flex items-center gap-1.5 text-sm text-[#404848]">
          <UIcon
            name="i-heroicons-building-office"
            class="w-3.5 h-3.5 text-gray-400 shrink-0"
          />
          <span>Naseej Digital Solutions</span>
        </div>
      </div>
    </div>

    <!-- Badges -->
    <div class="flex flex-wrap items-center gap-2">
      <div
        class="bg-[#f0fdfa] text-[#0f766e] px-3 py-1.5 rounded-lg flex items-center gap-1.5 text-[11px] font-bold"
      >
        <UIcon name="i-heroicons-star" class="w-3 h-3" />
        <span>3-5 Years</span>
      </div>
      <div
        class="bg-[#f3f4f3] text-[#506262] px-3 py-1.5 rounded-lg flex items-center gap-1.5 text-[11px] font-bold"
      >
        <UIcon name="i-heroicons-archive-box" class="w-3.5 h-3.5" />
        <span>Information Technology</span>
      </div>
      <div
        class="bg-[#f3f4f3] text-[#506262] px-3 py-1.5 rounded-lg flex items-center gap-1.5 text-[11px] font-bold"
      >
        <UIcon name="i-heroicons-clock" class="w-3.5 h-3.5" />
        <span>Full Time</span>
      </div>
    </div>

    <!-- Price & Date -->
    <div class="flex items-center justify-between pt-1">
      <div class="flex items-baseline gap-1.5">
        <span class="font-bold text-[#00383a] text-base">12,000 - 15,000</span>
        <span class="text-[10px] text-[#00383a] opacity-70">SAR</span>
      </div>
      <span class="text-[11px] text-[#707979]">Published 2 days ago</span>
    </div>

    <!-- Button -->
    <button
      class="w-full bg-[#00383a] cursor-pointer hover:bg-[#002122] text-white py-4 rounded-2xl text-base transition-colors mt-2"
    >
      Apply Now
    </button>
  </div>
</template>

<script setup lang="ts"></script>
