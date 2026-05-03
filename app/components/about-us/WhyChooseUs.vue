<script setup lang="ts">
//👉 Imports
import AboutData from "../icons/AboutData.vue";
import AboutSecure from "../icons/AboutSecure.vue";
import AboutSpeed from "../icons/AboutSpeed.vue";
import WhyIcon from "../icons/WhyIcon.vue";
</script>
<template>
  <div
    class="why-choose-us-container bg-white lg:py-30 sm:py-20 py-16 sm:px-6 px-4"
  >
    <!-- Header  -->
    <div
      class="why-choose-us_header flex flex-col items-center justify-center text-center sm:gap-6 gap-4"
    >
      <p class="font-bold text-[#115E59]">مميزاتنا الاستثنائية</p>
      <h2 class="lg:text-5xl sm:text-4xl text-2xl font-bold text-[#002122]">
        لماذا أدق هي خيارك الأول؟
      </h2>
      <p class="sm:text-lg text-base">
        نجمع بين التكنولوجيا المتطورة والفهم العميق لاحتياجات سوق العمل المحلي
      </p>
    </div>
    <!-- Content  -->
    <div
      :class="[
        'why-choose-us_content lg:mt-24 sm:mt-19 mt-16',
        'grid grid-cols-12 lg:gap-8 sm:gap-6 gap-4 items-start',
      ]"
    >
      <!-- Ai Section  -->
      <div class="ai-container md:col-span-8 col-span-12">
        <!-- Image  -->
        <img
          src="/imgs/about/why-choose.png"
          width="800"
          height="450"
          class="absolute inset-0 z-0 opacity-40 size-full object-cover sm:object-top-right object-center"
        />
        <!-- Overlay  -->
        <div
          class="absolute inset-0 z-10"
          style="
            background: linear-gradient(
              0deg,
              #f3f4f3 0%,
              rgba(243, 244, 243, 0.8) 50%,
              rgba(243, 244, 243, 0) 100%
            );
          "
        />
        <div class="ai-content flex flex-col gap-4 relative z-20">
          <div class="ai-content_icon-container">
            <WhyIcon />
          </div>
          <p class="lg:text-3xl sm:text-2xl text-xl font-bold text-[#002122]">
            تحليل الكفاءات بالذكاء الاصطناعي
          </p>
          <p class="lg:text-lg sm:text-base text-sm max-w-lg">
            نستخدم خوارزميات متقدمة لتحليل المهارات والملاءمة الثقافية بدقة تزيد
            عن 95% لضمان أفضل مطابقة.
          </p>
        </div>
      </div>
      <!-- Trust Section  -->
      <div
        class="trust-container lg:gap-14 sm:gap-10 gap-8 md:col-span-4 sm:col-span-6 col-span-12"
      >
        <div class="trust_icon-container">
          <AboutSecure />
        </div>
        <div class="space-y-4">
          <p class="lg:text-2xl sm:text-xl text-lg font-bold text-white">
            بيئة آمنة وموثوقة
          </p>
          <p class="lg:text-base sm:text-sm text-xs text-[#D4E6E6]">
            تشفير كامل للبيانات وحماية تامة لخصوصية المستخدمين والشركات وفق أعلى
            المعايير العالمية.
          </p>
        </div>
      </div>
      <!-- Speed Section  -->
      <div
        class="speed-container h-full md:col-span-4 sm:col-span-6 col-span-12"
      >
        <AboutSpeed />
        <p class="lg:text-2xl sm:text-xl text-lg font-bold text-[#002122]">
          سرعة التنفيذ القصوى
        </p>
        <p class="lg:text-base sm:text-sm text-xs max-w-lg">
          تقليص وقت التوظيف من أسابيع إلى أيام بفضل الأتمتة الذكية والعمليات
          الميسرة.
        </p>
      </div>
      <!-- Data Section  -->
      <div class="data-container h-full md:col-span-8 col-span-12">
        <div class="data_icon-container">
          <AboutData />
        </div>
        <p class="lg:text-2xl sm:text-xl text-lg font-bold text-[#002122]">
          إدارة الذاكرة المؤسسية
        </p>
        <p class="lg:text-lg sm:text-base text-sm max-w-lg">
          حفظ وتوثيق الخبرات والمهارات لضمان استمرارية المعرفة داخل مؤسستك حتى
          مع تغير الأجيال والفرق.
        </p>
      </div>
    </div>
  </div>
</template>
<style lang="scss">
.why-choose-us-container {
  .why-choose-us_content {
    .ai-container {
      position: relative;
      border-radius: 48px;
      border: 1px solid rgba(112, 121, 121, 0.05);
      background: #f3f4f3;
      overflow: hidden;
      padding: 30px;
      padding-top: 100px;
      .ai-content {
        .ai-content_icon-container {
          border-radius: 16px;
          background: white;
          box-shadow:
            0 10px 15px -3px rgba(0, 0, 0, 0.1),
            0 4px 6px -4px rgba(0, 0, 0, 0.1);
          display: flex;
          align-items: center;
          justify-content: center;
          width: 56px;
          height: 56px;
        }
      }
    }
    .trust-container {
      border-radius: 30px;
      background: #517f81;
      box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
      display: flex;
      flex-direction: column;
      padding: 30px;
      .trust_icon-container {
        border-radius: 16px;
        border: 1px solid rgba(255, 255, 255, 0.2);
        background: rgba(255, 255, 255, 0.1);
        backdrop-filter: blur(6px);
        display: flex;
        align-items: center;
        justify-content: center;
        width: 64px;
        height: 64px;
      }
    }
    .speed-container {
      display: flex;
      flex-direction: column;
      gap: 16px;
      border-radius: 48px;
      border: 1px solid rgba(112, 121, 121, 0.1);
      background: #fff;
      box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
      padding: 30px;
    }
    .data-container {
      border-radius: 48px;
      border: 1px solid rgba(112, 121, 121, 0.05);
      background: rgba(232, 232, 232, 0.5);
      padding: 30px;
      display: flex;
      flex-direction: column;
      gap: 16px;
      .data_icon-container {
        border-radius: 48px;
        border: 1px solid rgba(112, 121, 121, 0.05);
        background: rgba(232, 232, 232, 0.5);
        width: 46px;
        height: 46px;
        display: flex;
        align-items: center;
        justify-content: center;
      }
    }
    @media (min-width: 640px) {
      .ai-container {
        padding-top: 150px;
      }
    }
    @media (min-width: 1024px) {
      .ai-container {
        padding: 48px;
        padding-top: 210px;
      }
      .speed-container,
      .trust-container,
      .data-container {
        padding: 48px;
      }
    }
  }
}
</style>
