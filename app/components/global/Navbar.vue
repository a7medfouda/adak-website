<script lang="ts" setup>
const drawerOpen = ref(false);
const { t } = useI18n();

const authOverlayOpen = useState("authOverlayOpen", () => false);
const authStep = useState("authStep", () => "login");

const openAuth = (step: "login" | "register") => {
  authStep.value = step;
  authOverlayOpen.value = true;
};

// Mock Auth State
const isLoggedIn = useState("isLoggedIn", () => true);

const userMenu = [
  [{
    label: 'Profile',
    icon: 'i-heroicons-user',
    to: '/profile'
  }],
  [{
    label: 'Logout',
    icon: 'i-heroicons-arrow-left-on-rectangle',
    click: () => {
      isLoggedIn.value = false;
    }
  }]
];

const navLinks = [
  { label: "Home", to: "/" },
  { label: "Jobs", to: "/jobs" },
  { label: "Companies", to: "/companies" },
  { label: "About Platform", to: "/about" },
];
</script>

<template>
  <nav
    class="sticky top-0 z-50 bg-white border-b border-gray-100 shadow-sm h-16 md:h-20 flex items-center"
  >
    <SharedContainer class="w-full">
      <div class="flex items-center justify-between gap-4">
        <!-- Logo -->
        <NuxtLink to="/" class="shrink-0">
          <img src="/imgs/logo.svg" alt="ADAQ" class="h-8 md:h-10" />
        </NuxtLink>

        <!-- Desktop Links -->
        <ul class="hidden md:flex items-center gap-6 lg:gap-8">
          <li v-for="link in navLinks" :key="link.to">
            <NuxtLink
              :to="link.to"
              class="text-[#475569] hover:text-[#0F766E] transition-colors relative pb-1 whitespace-nowrap"
              active-class="after:absolute after:bottom-0 after:left-0 after:w-full after:h-0.5 after:bg-[#0F766E] after:rounded-t-sm !text-[#0F766E]"
            >
              {{ link.label }}
            </NuxtLink>
          </li>
        </ul>

        <!-- Right Actions -->
        <div class="flex items-center gap-3 md:gap-4">
          <template v-if="isLoggedIn">
            <!-- Notification -->
            <button class="relative p-2 text-[#292D32] hover:text-[#198078] transition-colors">
              <UIcon name="i-ph-bell" class="w-6 h-6" />
              <span class="absolute top-1 right-2 w-2 h-2 bg-red-600 rounded-full border border-white"></span>
            </button>
            
            <!-- Globe -->
            <UiLangSwitcher />

            <!-- User Menu -->
            <UDropdown :items="userMenu" :popper="{ placement: 'bottom-end' }">
              <div class="hidden md:flex items-center gap-2 bg-[#F4F6F8] hover:bg-[#E2E8F0] transition-colors rounded-full py-1.5 pl-1.5 pr-4 cursor-pointer">
                <img src="https://ui-avatars.com/api/?name=Kareem+Mohamed&background=198078&color=fff" alt="User" class="w-8 h-8 rounded-full object-cover" />
                <span class="text-sm font-bold text-[#154066]">Kareem Mohamed</span>
                <UIcon name="i-heroicons-chevron-down" class="w-4 h-4 text-gray-500" />
              </div>
            </UDropdown>
          </template>
          <template v-else>
            <UiLangSwitcher />

            <div class="hidden md:flex items-center">
              <UButton
                class="bg-[#198078] hover:bg-[#156e66] text-white rounded-[12px] px-5 lg:px-6 h-9 md:h-10 font-medium text-sm md:text-base"
                @click="openAuth('login')"
              >
                Login
              </UButton>
            </div>
          </template>

          <!-- Mobile Toggle -->
          <button
            class="md:hidden p-2 -mr-2 text-gray-600 focus:outline-none"
            @click="drawerOpen = true"
            aria-label="Toggle menu"
          >
            <UIcon name="i-heroicons-bars-3" class="w-6 h-6" />
          </button>
        </div>
      </div>
    </SharedContainer>
  </nav>

  <NavDrawer v-model:open="drawerOpen" />
</template>
