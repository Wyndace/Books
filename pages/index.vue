<template>
    <TheHero />
    <TheWhywe />
    <BookList title="Бестселлеры" filter="bestseller" />
    <BookList title="Недавно выпущенные" filter="native"/>
    <CardList title="Самые активные ветки форума" filter="?last_update"/>
    <CardList title="Новые ветки форума" filter='?date_created'/>
    <TheFAQ />
</template>

<script lang="ts" setup>
import TheHero from "~/components/sections/TheHero.vue"
import TheWhywe from "~/components/sections/TheWhywe.vue"
import BookList from "~/components/sections/BookList.vue"
import CardList from "~/components/sections/CardList.vue"
import TheFAQ from "~/components/sections/TheFAQ.vue"
definePageMeta({
  title: "Главная",
  description: "У нас вы найдете широкий выбор книг различных жанров и авторов, а также возможность обсудить их с другими любителями чтения.",
})  

</script>
