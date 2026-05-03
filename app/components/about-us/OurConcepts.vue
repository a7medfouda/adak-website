<script setup lang="ts">
//👉 Imports
import AboutEye from "../icons/AboutEye.vue";
import AboutFly from "../icons/AboutFly.vue";
</script>

<template>
  <div
    class="about-us_our-concepts grid sm:grid-cols-2 grid-cols-1 lg:gap-16 sm:gap-12 gap-10"
  >
    <div class="individual-concept">
      <div class="individual-concept_icon-container">
        <AboutEye  class="sm:size-11! size-9!"/>
      </div>
      <p
        class="individual-concept_title lg:text-3xl sm:text-2xl text-xl font-bold"
      >
        رؤيتنا
      </p>
      <p
        class="individual-concept_subtitle lg:text-lg sm:text-base text-sm font-light"
      >
        نسعى في "أدق" لأن نكون المحرك الرئيسي للتحول الرقمي في سوق العمل العربي،
        من خلال بناء مستقبل مهني مستدام يعتمد على البيانات الدقيقة والذكاء
        الاصطناعي لتمكين الأفراد والمؤسسات.
      </p>
    </div>
    <div class="individual-concept">
      <div class="individual-concept_icon-container">
        <AboutFly class="sm:size-11! size-9!"/>
      </div>
      <p
        class="individual-concept_title lg:text-3xl sm:text-2xl text-xl font-bold"
      >
        رسالتنا
      </p>
      <p
        class="individual-concept_subtitle lg:text-lg sm:text-base text-sm font-light"
      >
        رسالتنا هي جسر الفجوة بين الكفاءات الاستثنائية والشركات الطموحة، عبر
        توفير بيئة تقنية متقدمة تحفظ الذاكرة المؤسسية وتضمن اختيار الكادر الأمثل
        لكل دور وظيفي بسرعة وموثوقية.
      </p>
    </div>
  </div>
</template>
<style lang="scss">
.individual-concept {
  border-radius: 48px;
  border: 1px solid rgba(112, 121, 121, 0.05);
  background: #fff;
  box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
  padding: 24px;
  display: flex;
  flex-direction: column;
  gap: 16px;
  cursor: pointer;
  transition: all 0.3s ease;
  .individual-concept_icon-container {
    border-radius: 24px;
    background: rgba(209, 227, 228, 0.3);
    box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05) inset;
    color: #517f81;
    width: 60px;
    height: 60px;
    margin-bottom: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .individual-concept_title {
    color: #002122;
  }
  .individual-concept_subtitle {
    color: #404848;
  }
  &:hover {
    border: 1px solid rgba(255, 255, 255, 0.05);
    background: #321403;
    box-shadow:
      0 20px 25px -5px rgba(0, 0, 0, 0.1),
      0 8px 10px -6px rgba(0, 0, 0, 0.1);
    .individual-concept_icon-container {
      border-radius: 24px;
      background: rgba(195, 141, 115, 0.2);
      box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.05) inset;
      color: #c38d73;
    }
    .individual-concept_title {
      color: white;
    }
    .individual-concept_subtitle {
      color: #ffdbcb;
    }
  }
  @media (min-width: 640px) {
    padding: 32px;
    .individual-concept_icon-container {
      width: 80px;
      height: 80px;
      margin-bottom: 16px;
    }
  }
  @media (min-width: 1024px) {
    padding: 48px;
    gap: 24px;
  }
}
</style>
