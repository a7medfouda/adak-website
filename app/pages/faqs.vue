<script setup lang="ts">
//👉 Imports
import Container from "~/components/shared/Container.vue";
import Faq from "~/components/shared/Faq.vue";

//👉 Composables
const { t } = useI18n();

//👉 Meta
useHead({
  title: computed(() => `${t("Adak")} - ${t("FAQs")}`),
});
</script>

<template>
  <Container>
    <div class="lg:my-20 sm:my-14 my-10">
      <Faq />
    </div>
  </Container>
</template>
