<template>
  <div class="are-you-ready-container">
    <!-- Overlay Image -->
    <img
      src="/imgs/about/are-you-ready.png"
      class="absolute inset-0 z-0 size-full object-cover object-center"
    />
    <div class="are-you-ready_content">
      <h2
        class="lg:text-6xl sm:text-5xl text-3xl font-bold text-white max-w-[920px] leading-tight!"
      >
        هل أنت مستعد لتجربة الجيل القادم من التوظيف؟
      </h2>
      <p
        class="lg:text-xl sm:text-lg text-base font-light text-[#D4E6E6] max-w-3xl"
      >
        انضم إلى آلاف الشركات والمحترفين الذين يثقون في "أدق" لبناء مستقبلهم
        المهني المستدام.
      </p>
      <UButton block class="shared-button lg:mt-8 sm:mt-6 mt-4 w-fit"> ابدأ رحلتك معنا الآن</UButton>
    </div>
  </div>
</template>
<style lang="scss">
.are-you-ready-container {
  position: relative;
  background: #002122;
  padding: 48px;
  .are-you-ready_content {
    position: relative;
    z-index: 20;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    gap: 24px;
    margin: auto;
  }
  @media (min-width: 640px) {
    .are-you-ready_content {
      gap: 36px;
    }
    padding: 60px;
  }
  @media (min-width: 1024px) {
    .are-you-ready_content {
      gap: 48px;
    }
    padding: 96px;
  }
}
</style>
