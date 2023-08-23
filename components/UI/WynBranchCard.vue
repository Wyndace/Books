<template>
  <article class="bg-blue-500 px-8 py-4 gap-2 flex flex-col justify-between rounded-2xl">
    <div class="flex flex-col gap-2">
    <h3 class="text-base font-bold text-white text-center line-clamp-2">{{ branch.about.title }}</h3>
    <div class="flex flex-col gap-1">
      <p class="text-xs font-normal text-gray-200 w-full text-center">Количество сообщений: {{ branch.messages.length }}</p>
      <p class="text-xs font-normal text-gray-200 w-full text-center">Дата создания: {{ convertDate(new Date(branch.about.date_created)) }}</p>
      <p class="text-xs font-normal text-gray-200 w-full text-center">Количество сообщений: {{ branch.messages.length }}</p>
    </div>
    </div>
    <div class="flex gap-2">
      <WynButton typeBtn="solid" class="bg-red-400 rounded-lg px-11 py-3 text-white text-xs hover:bg-transparent border-red-400 border">
        <NuxtLink :to="branch.about.link">Посетить</NuxtLink> 
      </WynButton>
      <button class="bg-red-400 py-2 px-3 rounded-lg flex justify-center items-center hover:bg-transparent text-white border-red-400 border">
       <MarkIcon class="h-5 w-[14px]" /> 
      </button>
    </div>
  </article>
</template>

<script setup lang="ts">
import MarkIcon from "~/assets/images/icons/mark_outline.svg"
import WynButton from "~/components/UI/WynButton.vue"
interface Message extends Object {
    author: {
      link: string,
      img: string,
      full_name: string,
    },
    media: [
      { link: string, type: string }
    ]
    text: string,
    date: Date
}
interface Branch extends Object {
about: {
  title: string,
  link: string,
  date_created: Date
},
messages: Array<Message>,
  id: number,
}
  defineProps({
    branch: Object as () => Branch
  })
const convertDate = (date: Date) => {
  var yyyy = date.getFullYear().toString();
  var mm = (date.getMonth()+1).toString();
  var dd  = date.getDate().toString();

  var mmChars = mm.split('');
  var ddChars = dd.split('');

  return (ddChars[1]?dd:"0"+ddChars[0]) + '.' + (mmChars[1]?mm:"0"+mmChars[0]) + '.' + yyyy;
}
</script>
