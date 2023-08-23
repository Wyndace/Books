<template>
  <div class="flex flex-col min-h-screen">
    <SeoKit />
    <OgImageScreenshot />
    <TheHeader />
    <main>
      <slot />
    </main>
    <TheFooter />
  </div>
</template>

<script setup lang="ts">
  import TheHeader from "~/components/sections/TheHeader.vue"
  import TheFooter from "~/components/sections/TheFooter.vue"
</script>
