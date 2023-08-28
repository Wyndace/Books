<template>
  <WynSection>
<<<<<<< HEAD
    <WynContent class="flex flex-col justify-between items-stretch gap-9"> 
    <div class="flex justify-between items-center gap-1">
      <WynBadge>Частые вопросы</WynBadge>
    </div>
    <ul class="grid grid-cols-12 gap-3 w-full items-center">
      <li class="col-span-4">
        <WynAccoridon title="Почему такие низкие цены?" text="Мы обращаемся к издателям напрямую и ставим минимальный сервисный сбор за покупку через наш сайт." />
      </li>
      <li class="col-span-4">
        <WynAccoridon title="А Вы сможете доставить в город N?" text="Мы обращаемся к издателям напрямую и ставим минимальный сервисный сбор за покупку через наш сайт." />
      </li>
      <li class="col-span-4">
        <WynAccoridon title="Сколько занимает время доставки?" text="Мы обращаемся к издателям напрямую и ставим минимальный сервисный сбор за покупку через наш сайт." />
      </li>
      <li class="col-span-4">
        <WynAccoridon title="Какие методы оплаты Вы принимаете?" text="Мы обращаемся к издателям напрямую и ставим минимальный сервисный сбор за покупку через наш сайт." />
      </li>
      <li class="col-span-4">
        <WynAccoridon title="Что делать если меня оскорбили на форуме?" text="Мы обращаемся к издателям напрямую и ставим минимальный сервисный сбор за покупку через наш сайт." />
      </li>
    </ul>
=======
    <WynContent class="flex flex-col justify-between items-stretch gap-9">
      <div class="flex justify-between items-center gap-1">
        <WynBadge>Частые вопросы</WynBadge>
      </div>
      <div class="flex justify-between items-center">
        <ul class="flex flex-col w-[456px] items-center gap-3">
          <li class="col-span-4">
            <WynAccoridon
              title="Почему такие низкие цены?"
              text="Мы&nbsp;обращаемся к&nbsp;издателям напрямую и&nbsp;ставим минимальный сервисный сбор за&nbsp;покупку через наш сайт."
            />
          </li>
          <li class="col-span-4">
            <WynAccoridon
              title="А Вы сможете доставить в город N?"
              text="Мы&nbsp;обращаемся к&nbsp;издателям напрямую и&nbsp;ставим минимальный сервисный сбор за&nbsp;покупку через наш сайт."
            />
          </li>
          <li class="col-span-4">
            <WynAccoridon
              title="Сколько занимает время доставки?"
              text="Мы&nbsp;обращаемся к&nbsp;издателям напрямую и&nbsp;ставим минимальный сервисный сбор за&nbsp;покупку через наш сайт."
            />
          </li>
          <li class="col-span-4">
            <WynAccoridon
              title="Какие методы оплаты&nbsp;Вы принимаете?"
              text="Мы&nbsp;обращаемся к&nbsp;издателям напрямую и&nbsp;ставим минимальный сервисный сбор за&nbsp;покупку через наш сайт."
            />
          </li>
          <li class="col-span-4">
            <WynAccoridon
              title="Как вернуть деньги, если книга не понравилась?"
              text="Мы&nbsp;обращаемся к&nbsp;издателям напрямую и&nbsp;ставим минимальный сервисный сбор за&nbsp;покупку через наш сайт."
            />
          </li>
        </ul>
        <img
          class="w-[480px] h-[415px]"
          src="/images/faq.svg"
          alt="иконка вопросов"
        />
      </div>
>>>>>>> fe1d6c6 (moved to github)
    </WynContent>
  </WynSection>
</template>

<script setup lang="ts">
  import WynSection from "~/components/UI/WynSection.vue"
  import WynContent from "~/components/UI/WynContent.vue"
  import WynBadge from '~/components/UI/WynBadge.vue';
  import WynAccoridon from '~/components/UI/WynAccordion.vue';
</script>

