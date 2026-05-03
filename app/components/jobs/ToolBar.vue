<script setup lang="ts">
//👉 Props
const props = defineProps<{
  isLoading: boolean;
  cities: { label: string; value: string }[];
  inputUi: Record<string, string>;
}>();

//👉 Emits
defineEmits(["handle-search"]);

//👉 Data
const search = ref("");
const city = ref(props.cities[0]?.value || "");
</script>
<template>
  <div
    :class="[
      'tool-bar-container shared-container sm:p-6 p-4',
      'flex items-stretch gap-4',
    ]"
  >
    <!-- Search Input  -->
    <UInput
      v-model="search"
      icon="i-lucide-search"
      :placeholder="$t('search placeholder')"
      :disabled="isLoading"
      class="w-[40%]"
      :ui="{
        ...inputUi,
        base: inputUi?.base?.replace('h-auto', 'h-full'),
      }"
    />
    <!-- City Select  -->
    <USelect
      v-model="city"
      icon="proicons:location"
      :items="cities"
      :placeholder="$t('City')"
      :disabled="isLoading"
      class="w-[35%]"
      :ui="inputUi"
    />
    <UButton
      block
      icon="i-lucide-arrow-left"
      :loading="isLoading"
      :disabled="isLoading"
      :ui="{ base: 'flex-row-reverse', leadingIcon: 'ltr:-rotate-90' }"
      class="w-[25%] py-4 rounded-xl bg-[#0F766E] font-bold sm:text-base text-sm"
      @click="$emit('handle-search', { search: search, city: city })"
    >
      {{ $t("Search") }}
    </UButton>
  </div>
</template>
