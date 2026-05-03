<script setup lang="ts">
//👉 Data
const active = ref("0");

//👉 Computed
const faqItems = [
  {
    label: "كيف يمكنني التقديم على وظيفة؟",
    content:
      "الذاكرة المؤسسية هي قاعدة بيانات ذكية في أداء تخزن سجل التفاعلات والمهارات المطلوبة تاريخياً في الذاكرة المؤسسية هي قاعدة بيانات ذكية في أداء تخزن سجل التفاعلات والمهارات المطلوبة تاريخياً في",
  },
  {
    label: "ما هي الذاكرة المؤسسية؟",
    content:
      "الذاكرة المؤسسية هي قاعدة بيانات ذكية في أداء تخزن سجل التفاعلات والمهارات المطلوبة تاريخياً في الذاكرة المؤسسية هي قاعدة بيانات ذكية في أداء تخزن سجل التفاعلات والمهارات المطلوبة تاريخياً في",
  },
  {
    label: "كيف أقوم بتعديل بيانات شركتي؟",
    content:
      "الذاكرة المؤسسية هي قاعدة بيانات ذكية في أداء تخزن سجل التفاعلات والمهارات المطلوبة تاريخياً في الذاكرة المؤسسية هي قاعدة بيانات ذكية في أداء تخزن سجل التفاعلات والمهارات المطلوبة تاريخياً في",
  },
  {
    label: "هل منصة أداء مجانية للمرشحين؟",
    content:
      "الذاكرة المؤسسية هي قاعدة بيانات ذكية في أداء تخزن سجل التفاعلات والمهارات المطلوبة تاريخياً في الذاكرة المؤسسية هي قاعدة بيانات ذكية في أداء تخزن سجل التفاعلات والمهارات المطلوبة تاريخياً في",
  },
];
</script>
<template>
  <SharedContainer>
    <div class="faqs-container flex flex-col lg:gap-8 sm:gap-6 gap-4">
      <!-- Header  -->
      <div class="faqs_header space-y-2">
        <h2 class="lg:text-3xl sm:text-2xl text-xl font-bold text-[#002122]">
          الأسئلة الشائعة
        </h2>
        <p class="lg:text-base sm:text-sm text-xs">
          نحن في منصة ADAQ نلتزم بحماية خصوصية معلوماتك الشخصية وبياناتك.
        </p>
      </div>
      <!-- Content  -->
      <div class="faqs_content">
        <UAccordion
          v-model="active"
          :items="faqItems"
          :collapsible="false"
          :ui="{
            root: 'w-full space-y-4',
            item: [
              'faq-item bg-[#FFFFFF01] overflow-hidden border-0',
              ' data-[state=open]:overflow-visible',
            ],
            header: 'faq-header sm:py-5 sm:px-6 py-4 px-5 flex',
            trigger: [
              'group flex w-full items-center justify-between gap-3 cursor-pointer p-0',
            ],
            content: 'data-[state=open]:block',
            body: 'sm:pb-5 sm:px-6 pb-4 px-5 sm:text-base text-sm leading-relaxed',
            trailingIcon: [
              'shrink-0 size-5 transition-transform duration-200',
              'group-data-[state=open]:rotate-180',
            ],
            label:
              'text-start flex-1 text-[#002122] sm:text-lg text-base font-bold',
          }"
        />
      </div>
    </div>
  </SharedContainer>
</template>
<style lang="scss">
.faqs-container {
  .faqs_content {
    .faq-item {
      border-radius: 0 16px 16px 16px;
      background: rgba(255, 255, 255, 0);
      box-shadow:
        0 10px 30px -5px rgba(0, 0, 0, 0.04),
        0 4px 12px -2px rgba(0, 0, 0, 0.03);
    }
  }
}
</style>
