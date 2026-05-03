<template>
  <div class="min-h-screen bg-[#f9fafa] pt-32 pb-24">
    <SharedContainer>
      <!-- Details will be implemented here when Figma design is provided -->
      <div class="bg-white rounded-[24px] p-8 shadow-sm text-center">
        <h2 class="text-2xl font-bold text-[#002122] mb-4">Company Details Page</h2>
        <p class="text-[#506262]">
          Waiting for Figma design MCP context to implement this page.
          <br>
          Company ID: {{ route.params.id }}
        </p>
      </div>
    </SharedContainer>
  </div>
</template>

<script setup lang="ts">
const route = useRoute();

// TODO: Fetch company details based on route.params.id
</script>
