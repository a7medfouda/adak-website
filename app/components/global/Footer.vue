<script setup lang="ts">
const { t } = useI18n();
</script>

<template>
  <footer class="bg-[#F1F5F9] pt-16 pb-8 border-t border-[#E5E7EB]">
    <SharedContainer>
      <div
        class="grid grid-cols-1 md:grid-cols-12 gap-10 md:gap-8 mb-16 text-center md:text-start"
      >
        <!-- Logo & Description (Right side in Arabic, Left side in English) -->
        <div
          class="col-span-1 md:col-span-5 flex flex-col items-center md:items-start order-1 md:order-1"
        >
          <NuxtLink to="/" class="block mb-6">
            <img src="/imgs/logo.svg" alt="ADAQ" class="h-10 md:h-12" />
          </NuxtLink>
          <p
            class="text-[#475569] text-sm md:text-base leading-relaxed mb-8 max-w-sm"
          >
            The leading recruitment platform in the Arab region, connecting
            ambition with opportunities to build a sustainable institutional
            future.
          </p>
          <div class="flex items-center gap-3">
            <NuxtLink
              to="#"
              class="w-10 h-10 sm:w-12 sm:h-12 rounded-full bg-white flex items-center justify-center text-[#198078] hover:bg-[#198078] hover:text-white transition-colors shadow-sm"
            >
              <UIcon name="i-ph-instagram-logo-bold" class="w-5 h-5" />
            </NuxtLink>
            <NuxtLink
              to="#"
              class="w-10 h-10 sm:w-12 sm:h-12 rounded-full bg-white flex items-center justify-center text-[#198078] hover:bg-[#198078] hover:text-white transition-colors shadow-sm"
            >
              <UIcon name="i-ph-x-logo-bold" class="w-5 h-5" />
            </NuxtLink>
            <NuxtLink
              to="#"
              class="w-10 h-10 sm:w-12 sm:h-12 rounded-full bg-white flex items-center justify-center text-[#198078] hover:bg-[#198078] hover:text-white transition-colors shadow-sm"
            >
              <UIcon name="i-ph-linkedin-logo-bold" class="w-5 h-5" />
            </NuxtLink>
            <NuxtLink
              to="#"
              class="w-10 h-10 sm:w-12 sm:h-12 rounded-full bg-white flex items-center justify-center text-[#198078] hover:bg-[#198078] hover:text-white transition-colors shadow-sm"
            >
              <UIcon name="i-ph-envelope-simple-bold" class="w-5 h-5" />
            </NuxtLink>
          </div>
        </div>

        <!-- Platform Links -->
        <div
          class="col-span-1 md:col-span-3 flex flex-col items-center md:items-start order-2 md:order-2"
        >
          <h3 class="text-lg font-bold text-[#198078] mb-6">Platform</h3>
          <ul class="space-y-4">
            <li>
              <NuxtLink
                to="/about"
                class="text-[#475569] hover:text-[#198078] transition-colors text-sm md:text-base"
                >About Platform</NuxtLink
              >
            </li>
            <li>
              <NuxtLink
                to="#features"
                class="text-[#475569] hover:text-[#198078] transition-colors text-sm md:text-base"
                >Features</NuxtLink
              >
            </li>
            <li>
              <NuxtLink
                to="/jobs"
                class="text-[#475569] hover:text-[#198078] transition-colors text-sm md:text-base"
                >Available Jobs</NuxtLink
              >
            </li>
          </ul>
        </div>

        <!-- Support and Legal -->
        <div
          class="col-span-1 md:col-span-4 flex flex-col items-center md:items-start order-3 md:order-3"
        >
          <h3 class="text-lg font-bold text-[#198078] mb-6">Support & Legal</h3>
          <ul class="space-y-4">
            <li>
              <NuxtLink
                to="/privacy"
                class="text-[#475569] hover:text-[#198078] transition-colors text-sm md:text-base"
                >Privacy Policy</NuxtLink
              >
            </li>
            <li>
              <NuxtLink
                to="/terms"
                class="text-[#475569] hover:text-[#198078] transition-colors text-sm md:text-base"
                >Terms of Service</NuxtLink
              >
            </li>
            <li>
              <NuxtLink
                to="/faq"
                class="text-[#475569] hover:text-[#198078] transition-colors text-sm md:text-base"
                >FAQ</NuxtLink
              >
            </li>
            <li>
              <NuxtLink
                to="/contact"
                class="text-[#475569] hover:text-[#198078] transition-colors text-sm md:text-base"
                >Contact Us</NuxtLink
              >
            </li>
          </ul>
        </div>
      </div>

      <!-- Copyright Area -->
      <div class="flex items-center justify-center md:justify-end">
        <p class="text-xs md:text-sm text-[#64748B]">
          Designed & Developed By
          <a
            href="https://quarizm.com"
            target="_blank"
            class="text-[#198078] hover:text-[#156e66] transition-colors"
          >
            Quarizm Solutions
          </a>
        </p>
      </div>
    </SharedContainer>
  </footer>
</template>
