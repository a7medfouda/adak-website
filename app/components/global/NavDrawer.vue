<script lang="ts" setup>
import { computed, watch } from 'vue';
import { useRoute } from 'vue-router';

const props = defineProps<{ open: boolean }>();
const emit = defineEmits<{ "update:open": [value: boolean] }>();

const isOpen = computed({
  get: () => props.open,
  set: (val) => emit("update:open", val),
});

const close = () => (isOpen.value = false);

const authOverlayOpen = useState("authOverlayOpen", () => false);
const authStep = useState("authStep", () => "login");

const openAuth = (step: "login" | "register") => {
  authStep.value = step;
  authOverlayOpen.value = true;
  close();
};

// Mock Auth State
const isLoggedIn = useState("isLoggedIn", () => true);

const userMenu = [
  [{
    label: 'Profile',
    icon: 'i-heroicons-user',
    to: '/profile',
    click: close
  }],
  [{
    label: 'Logout',
    icon: 'i-heroicons-arrow-left-on-rectangle',
    click: () => {
      isLoggedIn.value = false;
      close();
    }
  }]
];

const navLinks = [
  { label: "Home", to: "/" },
  { label: "Jobs", to: "/jobs" },
  { label: "Companies", to: "/companies" },
  { label: "About Platform", to: "/about" },
];

const route = useRoute();
watch(() => route.path, close);
</script>

<template>
  <UDrawer
    v-model:open="isOpen"
    direction="right"
    class="md:hidden"
    :ui="{
      content: 'bg-white h-full flex flex-col w-[300px]',
      body: 'p-6 flex-1 flex flex-col',
      header: 'p-6 border-b border-gray-100 flex items-center justify-between',
    }"
  >
    <template #header>
      <NuxtLink to="/" @click="close">
        <img src="/imgs/logo.svg" alt="ADAQ" class="h-8" />
      </NuxtLink>
      <UButton
        icon="i-heroicons-x-mark"
        color="gray"
        variant="ghost"
        @click="close"
      />
    </template>

    <template #body>
      <nav class="flex flex-col gap-6">
        <NuxtLink
          v-for="link in navLinks"
          :key="link.to"
          :to="link.to"
          class="text-lg font-bold text-[#475569] hover:text-[#0F766E] transition-colors"
          active-class="text-[#0F766E]"
          @click="close"
        >
          {{ link.label }}
        </NuxtLink>
      </nav>

      <div class="mt-auto pt-8 border-t border-gray-100 flex flex-col gap-6">
        <template v-if="isLoggedIn">
          <!-- Notification & LangSwitcher -->
          <div class="flex items-center justify-between">
            <button class="flex items-center gap-2 text-[#292D32] hover:text-[#198078] transition-colors">
              <div class="relative p-2">
                <UIcon name="i-ph-bell" class="w-6 h-6" />
                <span class="absolute top-1 right-2 w-2 h-2 bg-red-600 rounded-full border border-white"></span>
              </div>
              <span class="font-medium">Notifications</span>
            </button>
            <UiLangSwitcher />
          </div>

          <!-- User Profile Dropdown -->
          <UDropdown :items="userMenu" :popper="{ placement: 'top-end' }" class="w-full">
            <div class="flex items-center justify-between w-full bg-[#F4F6F8] hover:bg-[#E2E8F0] transition-colors rounded-xl p-3 cursor-pointer border border-gray-100">
              <div class="flex items-center gap-3">
                <img src="https://ui-avatars.com/api/?name=Kareem+Mohamed&background=198078&color=fff" alt="User" class="w-10 h-10 rounded-full object-cover" />
                <span class="font-bold text-[#154066]">Kareem Mohamed</span>
              </div>
              <UIcon name="i-heroicons-chevron-down" class="w-5 h-5 text-gray-500" />
            </div>
          </UDropdown>
        </template>
        
        <template v-else>
          <div class="flex items-center justify-between">
            <span class="text-[#475569] font-medium">Language</span>
            <UiLangSwitcher />
          </div>
          <div class="flex flex-col gap-3">
            <UButton block class="bg-[#198078] hover:bg-[#156e66] text-white rounded-[12px] h-12 font-medium text-lg flex justify-center" @click="openAuth('login')">
              Login
            </UButton>
            <UButton block variant="outline" class="border-[#198078] text-[#198078] hover:bg-[#198078]/5 rounded-[12px] h-12 font-medium text-lg flex justify-center" @click="openAuth('register')">
              Get Started
            </UButton>
          </div>
        </template>
      </div>
    </template>
  </UDrawer>
</template>
