<template>
  <div class="flex gap-2 items-center">
  <div class="relative">
    <div :style="{width: rating/5*100 + '%', 'mask-image': 'url(\'' + StarLogoPath + '\')', '-webkit-mask-image': 'url(\'' + StarLogoPath + '\')'}" class="absolute top-0 left-[-0.1px] mask-star overflow-hidden h-4 bg-amber-400"></div>
    <div class="flex justify-between gap-1"> 
      <StarLogo class="h-4 w-4 text-gray-600"/>
      <StarLogo class="h-4 w-4 text-gray-600"/>
      <StarLogo class="h-4 w-4 text-gray-600"/>
      <StarLogo class="h-4 w-4 text-gray-600"/>
      <StarLogo class="h-4 w-4 text-gray-600"/>
    </div>
  </div> 
  <p class="text-gray-600 text-sm font-normal">({{ reviews }})</p>
  </div>
</template>


<script setup lang="ts">
  import StarLogo from "~/assets/images/icons/star.svg"
  import StarLogoPathRaw from "~/assets/images/icons/stars.svg?1"
  const StarLogoPath = StarLogoPathRaw.replace('?1', '')
  defineProps({
    rating: Number,
    reviews: Number
  })

</script>

<style scoped>
.mask-star {
  mask-repeat: repeat;
}
</style>
