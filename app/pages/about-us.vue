<script setup lang="ts">
//👉 Imports
import AreYouReady from "~/components/about-us/AreYouReady.vue";
import OurConcepts from "~/components/about-us/OurConcepts.vue";
import WhyChooseUs from "~/components/about-us/WhyChooseUs.vue";
import Container from "~/components/shared/Container.vue";

//👉 Composables
const { t } = useI18n();

//👉 Meta
useHead({
  title: computed(() => `${t("Adak")} - ${t("About Us")}`),
});
</script>

<template>
  <div class="about-us-container flex flex-col lg:my-20 sm:my-14 my-10">
    <Container>
      <!-- Concepts  -->
      <OurConcepts class="lg:mb-20 sm:mb-14 mb-10" />
    </Container>
    <!-- Why Choose Us  -->
    <WhyChooseUs />
    <!-- Are You Ready  -->
    <AreYouReady />
  </div>
</template>
