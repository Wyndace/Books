<template>
  <WynSection>
    <WynContent class="flex flex-col gap-9">
      <WynBadge>Почему мы?</WynBadge>
      <ul class="grid grid-cols-12 gap-8">
        <li class="p-4 col-span-4 rounded-3xl bg-blue-500 flex items-center flex-col justify-stretch">
          <div class="p-4 rounded-xl w-fit h-fit bg-red-400 mb-3"> 
            <BookIcon class="!h-5 !w-5 text-white"/>
          </div>
          <h3 class="text-white font-black text-center text-lg mb-2">Эксклюзивный контент</h3>
          <p class="text-gray-200 text-base font-normal text-center w-full">Наши постоянные партнеры — знаменитые издательства и авторы, что позволяет нам предоставлять эксклюзивные книги и редкие издания для наших пользователей</p>
        </li>
        <li class="p-4 rounded-3xl col-span-4 bg-blue-500 flex items-center flex-col justify-stretch">
          <div class="p-4 rounded-xl w-fit h-fit bg-red-400 mb-3"> 
            <MoneyIcon class="!h-5 !w-5 text-white"/>
          </div>
          <h3 class="text-white font-black text-center text-lg mb-2">Гибкая система оплаты и доставки</h3>
          <p class="text-gray-200 text-base text-center font-normal w-full">Выбирайте самый удобный для Вас способ оплаты и доставки, будь то онлайн-транзакция, оплата при получении</p>
        </li>
        <li class="p-4 rounded-3xl col-span-4 bg-blue-500 flex items-center flex-col justify-stretch">
          <div class="p-4 rounded-xl w-fit h-fit bg-red-400 mb-3"> 
            <ChatIcon class="!h-5 !w-5 text-white"/>
          </div>
          <h3 class="text-white font-black text-center text-lg mb-2">Живые обсуждения</h3>
          <p class="text-gray-200 text-base text-center font-normal w-full">Присоединяйтесь к нашему форуму, участвуйте в живых дискуссиях, чате и на прямых трансляциях с авторами, организованных специально для членов нашего сообщества</p>
        </li>
      </ul>
    </WynContent>
  </WynSection>
</template>

<script setup lang="ts">
import WynSection from "~/components/UI/WynSection.vue"
import WynContent from "~/components/UI/WynContent.vue"
import WynBadge from '~/components/UI/WynBadge.vue';
import BookIcon from '~/assets/images/icons/exclusive.svg'
import MoneyIcon from '~/assets/images/icons/money.svg'
import ChatIcon from '~/assets/images/icons/chat.svg'
</script>

