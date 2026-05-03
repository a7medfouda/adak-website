<template>
  <section class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-24">
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-16 items-center">
      <!-- Images -->
      <div class="relative h-[400px] sm:h-[500px] lg:h-[450px] mt-8 lg:mt-0">
        <!-- Blur effect -->
        <div
          class="absolute -top-4 -end-4 w-64 h-64 bg-[#d4e6e6]/50 blur-3xl rounded-full"
        />

        <div class="grid grid-cols-2 gap-4 h-full relative z-10 items-center">
          <!-- Image 1 -->
          <div
            class="relative w-full h-[70%] mt-[15%] rounded-2xl overflow-hidden shadow-xl"
          >
            <img
              src="https://images.unsplash.com/photo-1556761175-5973dc0f32e7?w=800&q=80"
              alt="Professional interaction"
              class="absolute inset-0 w-full h-full object-cover"
            />
          </div>
          <!-- Image 2 (Shifted down) -->
          <div
            class="relative w-full h-[70%] rounded-2xl overflow-hidden shadow-xl"
          >
            <img
              src="https://images.unsplash.com/photo-1600880292203-757bb62b4baf?w=800&q=80"
              alt="Team meeting"
              class="absolute inset-0 w-full h-full object-cover"
            />
          </div>
        </div>
      </div>
      <!-- Text Content -->
      <div class="flex flex-col gap-6">
        <!-- Tag -->
        <div
          class="flex items-center gap-2 self-start bg-[#4c2814] px-3 py-1.5 rounded-lg"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="12"
            height="12"
            viewBox="0 0 12 12"
            fill="none"
          >
            <path
              d="M3.5 9.33333L5.83333 7.55417L8.16667 9.33333L7.29167 6.44583L9.625 4.78333H6.76667L5.83333 1.75L4.9 4.78333H2.04167L4.375 6.44583L3.5 9.33333ZM5.83333 11.6667C5.02639 11.6667 4.26806 11.5135 3.55833 11.2073C2.84861 10.901 2.23125 10.4854 1.70625 9.96042C1.18125 9.43542 0.765625 8.81806 0.459375 8.10833C0.153125 7.39861 0 6.64028 0 5.83333C0 5.02639 0.153125 4.26806 0.459375 3.55833C0.765625 2.84861 1.18125 2.23125 1.70625 1.70625C2.23125 1.18125 2.84861 0.765625 3.55833 0.459375C4.26806 0.153125 5.02639 0 5.83333 0C6.64028 0 7.39861 0.153125 8.10833 0.459375C8.81806 0.765625 9.43542 1.18125 9.96042 1.70625C10.4854 2.23125 10.901 2.84861 11.2073 3.55833C11.5135 4.26806 11.6667 5.02639 11.6667 5.83333C11.6667 6.64028 11.5135 7.39861 11.2073 8.10833C10.901 8.81806 10.4854 9.43542 9.96042 9.96042C9.43542 10.4854 8.81806 10.901 8.10833 11.2073C7.39861 11.5135 6.64028 11.6667 5.83333 11.6667ZM5.83333 10.5C7.13611 10.5 8.23958 10.0479 9.14375 9.14375C10.0479 8.23958 10.5 7.13611 10.5 5.83333C10.5 4.53056 10.0479 3.42708 9.14375 2.52292C8.23958 1.61875 7.13611 1.16667 5.83333 1.16667C4.53056 1.16667 3.42708 1.61875 2.52292 2.52292C1.61875 3.42708 1.16667 4.53056 1.16667 5.83333C1.16667 7.13611 1.61875 8.23958 2.52292 9.14375C3.42708 10.0479 4.53056 10.5 5.83333 10.5Z"
              fill="#C38D73"
            />
          </svg>
          <span class="text-[#c38d73] text-sm">About Adak Platform</span>
        </div>

        <!-- Title -->
        <h2
          class="text-2xl sm:text-3xl lg:text-4xl font-black text-[#002122] leading-tight"
        >
          Leading Recruitment through Digital Innovation
        </h2>

        <!-- Description -->
        <p class="text-[#506262] text-sm sm:text-base leading-relaxed">
          At 'Adak', we believe that recruitment is not just filling vacancies, but an investment in human capital. We strive to provide an integrated digital environment that ensures transparency, accuracy, and speed in selecting talents that contribute to the growth of your organization.
        </p>

        <!-- Points List -->
        <ul class="flex flex-col gap-4 mt-2">
          <li class="flex items-center gap-3">
            <UIcon
              name="i-heroicons-check-circle-20-solid"
              class="w-6 h-6 text-teal-600 shrink-0"
            />
            <span class="text-[#1a1c1c] font-bold text-sm sm:text-base">AI technologies for job matching</span>
          </li>
          <li class="flex items-center gap-3">
            <UIcon
              name="i-heroicons-check-circle-20-solid"
              class="w-6 h-6 text-teal-600 shrink-0"
            />
            <span class="text-[#1a1c1c] font-bold text-sm sm:text-base">Integrated corporate memory management</span>
          </li>
          <li class="flex items-center gap-3">
            <UIcon
              name="i-heroicons-check-circle-20-solid"
              class="w-6 h-6 text-[#369689] shrink-0"
            />
            <span class="text-[#1a1c1c] font-bold text-sm sm:text-base">Customized solutions for large and startup companies</span>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script setup>
const { t } = useI18n();
</script>
