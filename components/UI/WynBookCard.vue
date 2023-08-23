<template>
  <article class="flex flex-col gap-2">
    <div class="flex flex-col gap-3">
      <NuxtLink :to="book?.about.link" class="w-[185px]">
        <img class="rounded-lg" :src="book?.about.img" :alt="book?.about.title">
      </NuxtLink>
      <div class="flex flex-col justify-start items-stretch gap-1">
        <div class="flex flex-col">
          <span :class="{ crossed: 'old_value' in book.price }"
            class="relative text-xs font-normal text-gray-600 h-4 w-fit">
            {{ book.price.old_value ? book.price.old_value : '' }} {{ book.price.old_value ? book.price.currency : '' }}
          </span>
          <span class="text-red-400 text-base font-bold">
            {{ book.price.value }} {{ book.price.currency }}
          </span>
        </div>
        <div class="flex flex-col gap-1">
          <h3 class="font-bold text-base text-slate-900 h-12 text-ellipsis line-clamp-2 overflow-hidden hover:underline">
            <NuxtLink :to="book.about.link">{{ book.about.title }}</NuxtLink>
          </h3>
          <p class="font-normal text-xs text-gray-600 h-full text-ellipsis line-clamp-2 overflow-hidden hover:underline">
            <NuxtLink :to="book.author.link">{{ book.author.full_name }}</NuxtLink>
          </p>
        </div>
      </div>
    </div>
    <div class="flex flex-col gap-3">
      <WynStars :rating="book?.rating" :reviews="book?.reviews" />
    </div>
    <div class="flex gap-2">
      <WynButton typeBtn="solid"
        class="bg-red-400 rounded-lg px-11 py-3 text-xs hover:bg-transparent hover:text-red-400 border-red-400 border">
        Купить</WynButton>
      <button
        class="bg-red-400 py-2 px-3 rounded-lg flex justify-center items-center hover:bg-transparent text-white hover:text-red-400 border-red-400 border">
        <MarkIcon class="h-5 w-[14px]" />
      </button>
    </div>
  </article>
</template>

<script setup lang="ts">
import WynStars from '~/components/UI/WynStars.vue'
import WynButton from "~/components/UI/WynButton.vue"
import MarkIcon from "~/assets/images/icons/mark_outline.svg"

interface Book extends Object {
  price: {
    old_value: number,
    value: number,
    currency: '₽'
  },
  about: {
    title: string,
    link: string,
    img: string
  },
  author: {
    full_name: string,
    link: string
  },
  rating: number,
  reviews: number,
  id: number,
}

defineProps({
  book: Object as () => Book
})
</script>

<style scoped>
.crossed::before {
  content: "";
  @apply absolute inset-y-0 inset-x-0 w-full h-1/2 border-b-red-400 border-b -rotate-12;
}
</style>
