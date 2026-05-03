<script lang="ts" setup>
import useI18nHandler from "~/composables/useI18nHandler";
const { t } = useI18n();
const { switchLang, langCookie, refreshing } = useI18nHandler();

const handleLanguageSwitch = () => {
  const newLang = langCookie.value === "en" ? "ar" : "en";
  switchLang(newLang);
};

// Logic: If current is EN, show "ع". If current is AR, show "EN".
const buttonLabel = computed(() => {
  return langCookie.value === "en" ? "ع" : "EN";
});

// Readable accessible label.
const ariaLabel = computed(() => {
  return langCookie.value === "en"
    ? t("Switch to Arabic")
    : t("Switch to English");
});
</script>

<template>
  <button
    :disabled="refreshing"
    :aria-busy="refreshing"
    :aria-label="ariaLabel"
    :title="ariaLabel"
    class="cursor-pointer flex items-center justify-center text-[#292D32] hover:text-[#198078] transition-colors"
    @click="handleLanguageSwitch"
  >
    <ClientOnly>
      <UIcon name="i-ph-globe" class="w-6 h-6" />
      <template #fallback>
        <UIcon name="i-ph-globe" class="w-6 h-6" />
      </template>
    </ClientOnly>
  </button>

  <!-- Full-screen Loading Overlay during language switch -->
  <ClientOnly>
    <Teleport to="body">
      <Transition
        enter-active-class="transition duration-500 ease-out"
        enter-from-class="opacity-0"
        enter-to-class="opacity-100"
        leave-active-class="transition duration-300 ease-in"
        leave-from-class="opacity-100"
        leave-to-class="opacity-0"
      >
        <div
          v-if="refreshing"
          class="fixed inset-0 z-[99999] flex flex-col items-center justify-center bg-[#154066]/90 backdrop-blur-md"
        >
          <div class="relative flex items-center justify-center mb-10">
            <!-- Glowing ambient background -->
            <div
              class="absolute w-32 h-32 bg-white/10 rounded-full blur-2xl animate-pulse"
            ></div>

            <!-- Outer Ring -->
            <div
              class="absolute w-20 h-20 border-[3px] border-white/10 border-t-white/90 rounded-full animate-[spin_1s_linear_infinite]"
            ></div>

            <!-- Inner Ring -->
            <div
              class="absolute w-14 h-14 border-[3px] border-white/10 border-b-white/80 rounded-full animate-[spin_1.5s_linear_infinite_reverse]"
            ></div>

            <!-- Center subtle dot -->
            <div
              class="w-3 h-3 bg-white/90 rounded-full animate-[ping_2s_cubic-bezier(0,0,0.2,1)_infinite]"
            ></div>
          </div>

          <div class="flex flex-col items-center space-y-4 opacity-95">
            <p
              class="text-white/90 text-2xl font-light tracking-widest uppercase"
            >
              Changing Language
            </p>
            <div
              class="w-16 h-[2px] bg-gradient-to-r from-transparent via-white/50 to-transparent rounded-full"
            ></div>
            <p
              class="text-white/90 text-2xl font-medium tracking-wide"
              dir="rtl"
            >
              جاري تغيير اللغة ...
            </p>
          </div>
        </div>
      </Transition>
    </Teleport>
  </ClientOnly>
</template>
