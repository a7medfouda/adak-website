<script setup lang="ts">
//👉 Imports
import ContactEmail from "~/components/icons/ContactEmail.vue";
import ContactPhone from "~/components/icons/ContactPhone.vue";
import ContactWhatsapp from "~/components/icons/ContactWhatsapp.vue";
import Container from "~/components/shared/Container.vue";
</script>
<template>
  <Container>
    <div
      class="contact-us-container flex flex-col lg:gap-8 sm:gap-6 gap-4 lg:my-20 sm:my-14 my-10"
    >
      <!-- Header  -->
      <div class="contact-us_header space-y-2">
        <h2 class="lg:text-3xl sm:text-2xl text-xl font-bold text-[#002122]">
          اتصل بنا
        </h2>
        <p class="lg:text-base sm:text-sm text-xs">
          نحن في منصة ADAQ نلتزم بحماية خصوصية معلوماتك الشخصية وبياناتك.
        </p>
      </div>
      <!-- Content  -->
      <div
        class="contact-us_content grid lg:grid-cols-3 sm:grid-cols-2 grid-cols-1 gap-4"
      >
        <div class="contact-us_card">
          <div class="contact-us_card_icon-container bg-[#25D3661A]">
            <ContactWhatsapp />
          </div>
          <p class="sm:text-base font-bold text-[#002122]">+966 50 123 4567</p>
          <p class="sm:text-sm text-xs">
            تواصل سريع ومباشر
          </p>
        </div>
        <div class="contact-us_card">
          <div class="contact-us_card_icon-container bg-[#00383A1A]">
            <ContactPhone />
          </div>
          <p class="sm:text-base font-bold text-[#002122]">+966 50 123 4567</p>
          <p class="sm:text-sm text-xs">
            الأحد - الخميس (9ص - 5م)
          </p>
        </div>
        <div
          class="contact-us_card sm:col-span-2 lg:col-span-1 sm:mx-auto sm:w-full"
        >
          <div class="contact-us_card_icon-container bg-[#4C28141A]">
            <ContactEmail />
          </div>
          <p class="sm:text-base font-bold text-[#002122]">support@adaq.sa</p>
          <p class="sm:text-sm text-xs">
            نرد خلال أقل من 24 ساعة
          </p>
        </div>
      </div>
    </div>
  </Container>
</template>
<style lang="scss">
.contact-us_content {
  .contact-us_card {
    border-radius: 0 16px 16px 16px;
    background: rgba(255, 255, 255, 0);
    box-shadow:
      0 10px 30px -5px rgba(0, 0, 0, 0.04),
      0 4px 12px -2px rgba(0, 0, 0, 0.03);
    padding: 16px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 4px;
    .contact-us_card_icon-container {
      width: 48px;
      height: 48px;
      margin-bottom: 12px;
      border-radius: 9999px;
      display: flex;
      justify-content: center;
      align-items: center;
    }
  }
  @media (min-width: 640px) {
    .contact-us_card {
      padding: 24px;
    }
  }
}
</style>
