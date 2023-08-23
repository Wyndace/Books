<template>
  <ul class="flex gap-7">
    <li class="font-medium" v-for="item in urls" :key="item.slug">
      <NuxtLink class="text-gray-600 hover:text-red-400 transition-colors duration-300" :to="item.slug" active-class="!text-red-400">{{ item.name }}</NuxtLink>
    </li>
  </ul>
</template>

<script setup lang="ts">
const urls = [
  { slug: "/", name: "Главная" },
  { slug: "/forum", name: "Форум" },
  { slug: "/books", name: "Все книги" },
  { slug: "/books/new", name: "Новинки" },
  { slug: "/books/popularity", name: "Популярное" },
  { slug: "/books/native", name: "Отечественное" },
]
</script>

<style scoped></style>
