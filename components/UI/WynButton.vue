<template>
  <button type="button" class="transition-colors duration-300" :class="typeBtn === 'solid' ? solidStyles : typeBtn === 'outline' ? outlineStyles : ''">
    <slot></slot>
  </button>
</template>

<script setup lang="ts">
defineProps({
  typeBtn: String,
})
const solidStyles = "text-white bg-blue-500 text-base hover:bg-red-400 text-center py-3"
const outlineStyles = "bg-transparent border-blue-500 text-base border-2 text-blue-500 py-3 hover:border-red-400 hover:text-red-400"
</script>
