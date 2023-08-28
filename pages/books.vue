<template>
  <TheSearch />
  <TheBooksFilters />
</template>

<script lang="ts" setup>
import TheSearch from "~/components/sections/TheSearch.vue"
import TheBooksFilters from "~/components/sections/TheBooksFilter.vue"
definePageMeta({
  title: "About",
  description: "Abot page of Nuxt Site",
})
</script>
