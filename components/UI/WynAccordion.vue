<template>
  <article class="rounded-3xl bg-blue-500 transition-[border-radius] duration-75 text-white" @click="open"
    aria-expanded="false">
    <button
      class="flex items-center justify-center w-full h-24 rounded-3xl p-6 gap-3 transition-[border-radius] duration-75">
      <h3 class="text-base font-black">{{ title }}</h3>
      <AccordionIcon class="!w-5 !h-5 !mb-0 transition-transform duration-75" />
    </button>
    <p class="max-h-0 opacity-0 duration-75 w-full text-center overflow-hidden px-6" aria-hidden="true">{{ text }}</p>
  </article>
</template>

<script setup lang="ts">
import AccordionIcon from "~/assets/images/icons/circle_arrow.svg"
defineProps({
  title: String,
  text: String,
})

const open = (e: any) => {
  const item = e.currentTarget,
    content = item.closest("article").querySelector("p")
  item.closest('article').classList.toggle("open")
  if (item.closest('article').classList.contains("open")) {
    item.setAttribute("aria-expanded", !0)
    content.setAttribute("aria-hidden", !1)
    content.style.maxHeight = content.scrollHeight + 24 + "px"
  } else {
    item.setAttribute("aria-expanded", !1)
    content.setAttribute("aria-hidden", !0)
    content.style.maxHeight = null
  }
}
</script>

<style scoped>
.open svg {
  @apply rotate-180
}

.open p {
  @apply opacity-100 pt-0 py-6
}

.accordion__control.focus-visible {
  outline: 2px dashed var(--white-color);
  outline-offset: 3px
}
</style>
