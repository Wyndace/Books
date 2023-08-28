<template>
  <WynSection>
    <WynContent class="group">
      <div class="w-full flex rounded-3xl border-blue-500 border-4 border-solid text-white transition-colors duration-300"
        :class="isButtonHovered ? 'border-red-400' : ''">
        <WynInput class="rounded-3xl" typeInput="text" hintInput="Введите автора, артикул, название..." nameInput="search"
          idInput="bookSearch" v-model.trim.lazy="formData.email.value" />
        <WynButton type-btn="solid" @mouseenter="isButtonHovered = true" @mouseleave="isButtonHovered = false"
          class="px-11 py-3 rounded-2xl">Найти</WynButton>
      </div>
    </WynContent>
  </WynSection>
</template>

<script setup lang="ts">
import WynSection from "~/components/UI/WynSection.vue"
import WynInput from "~/components/UI/WynInput.vue"
import WynContent from "~/components/UI/WynContent.vue"
import WynButton from "~/components/UI/WynButton.vue"
import { ref } from "vue"

const isButtonHovered = ref(false)

const formData = {
  email: ref(""),
  password: ref(""),
  visiblePass: ref(false),
}
</script>
