<template>
  <WynSection>
    <WynContent class="flex flex-col gap-9">
    <div class="flex justify-between items-center gap-1">
      <WynBadge>{{ title }}</WynBadge>
      <div class="flex gap-2">
      </div>
    </div>
      <ul class="grid grid-cols-12 gap-8" v-for="theme in Themes" :key="theme.id">
        <li v-for="branch in theme.branches" :key="branch.id" class="col-span-3 gap-8 h-full">
          <WynBranchCard class="h-full" :branch="branch" />
        </li>
      </ul>
    </WynContent>
  </WynSection>
</template>


<script setup lang="ts">
  import WynSection from "~/components/UI/WynSection.vue"
  import WynContent from "~/components/UI/WynContent.vue"
  import WynBadge from '~/components/UI/WynBadge.vue';
  import WynBranchCard from "~/components/UI/WynBranchCard.vue"
  defineProps({
    title: String,
    filter: String,
  })
const messages = [
{
      author: {
        id: 0,
        link: "https://vk.com/zjoida",
        img: '/sources/users/0.png',
        full_name: 'УЖики',
        nickname: 'zjoida'
      },
      media: [],
      text: 'Как Жожеку без лишних слов и телодвижений показать, что он Жожек?\nВо-первых, можно купить “Тайна Жожеков с красной планеты”, но ведь не будете же Вы таскать с собой книгу везде и всюду, верно?\nДжинсовка это слишком сложно и круто, так что остается один из немногих вариантов — значок!\nПотратив пару часов под «Выжигатель мозга» удалось сделать вот такие значки, один из которых уже красуется на рюкзаке.',
      date: new Date('2023-06-03')
  },
{
      author: {
        id: 1,
        link: "/users/1",
        img: '/sources/users/1.png',
        full_name: 'Александр Васильев',
        nickname: 'Wyndace'
      },
      media: [],
      text: 'Блин, суперские значки, респект! Ещё раз, к какой книге они в подарок идут? Они же ведь идут точно идут вместе с книгой «Тайна Жожеков с красной планеты»?',
      date: new Date('2023-06-03')
  }
  ]
const Themes = [
{
  title: 'Новости',
  id: '1',
  branches: [
  {
  about: {
    title: 'Тюменские Жожеки',
    link: '/forum/1/1',
    date_created: Date()
  },
  messages: messages,
    id: 1,
    theme_id: 1
  },
  {
  about: {
    title: 'Любители паранормальщины',
    link: '/forum/1/2',
    date_created: Date()
  },
  messages: messages,
    id: 2,
    theme_id: 1,
    locked: true
  },
  ]
}
]

</script>

