<template>
  <WynSection>
    <WynContent class="grid grid-cols-12">
      <div class="col-span-4 bg-blue-400 rounded-xl p-4 text-white font-bold">
        <form class="flex flex-col gap-6 w-full">
          <div class="flex flex-col gap-3">
            <h2 class="text-xl">Точечная подборка</h2>
            <div class="flex flex-col gap-3">
              <div class="flex flex-col gap-2">
                <div
                  class="flex relative after:absolute after:left-0 after:top-0 after:w-0.5 after:h-6 after:transform after:bg-white after:-translate-x-1/2 after:-translate-y-1/2">
                  <WynInput type-input="number" id-input="minPrice" name-input="minPrice" hint-input="0"
                    :model-value="formData.minPrice.value" class="rounded-s-xl border-e-0" :class="priceInputStyle" />
                  <WynInput type-input="number" id-input="minPrice" name-input="minPrice" hint-input="0"
                    :model-value="formData.minPrice.value" class="rounded-s-xl border-e-0" :class="priceInputStyle" />
                </div>
              </div>
            </div>
          </div>
        </form>
      </div>
    </WynContent>
  </WynSection>
</template>

<script setup lang="ts">
const priceInputStyle = "border-2 w-1/2 h-1/2 text-center text-white font-bold"

import WynSection from "~/components/UI/WynSection.vue"
import WynContent from "~/components/UI/WynContent.vue"
import WynInput from "~/components/UI/WynInput.vue"
import { ref } from "vue"

const formData = {
  minPrice: ref("0"),
}
</script>
