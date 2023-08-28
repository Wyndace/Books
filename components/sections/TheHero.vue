<template>
  <WynSection>
    <WynContent class="flex justify-between items-stretch">
      <div class="w-[555px] flex flex-col gap-10">
        <div>
          <h1 class="text-3xl font-medium text-slate-900 mb-5">
            Погрузись в&nbsp;увлекательный мир книг с&nbsp;нашим книжным
            магазином!
          </h1>
        </div>
        <form method="POST" class="bg-blue-500 py-7 px-5 flex flex-col justify-between rounded-3xl gap-5">
          <div class="flex flex-col justify-between gap-1">
            <div class="flex gap-4 text-center flex-col">
              <h2 class="text-xl font-black text-white">
                Присоединяйся к нам!
              </h2>
              <p class="text-base font-medium text-gray-200">
                Дабы не упустить возможность пополнить свою книжную коллекцию и
                найти однодумцев!
              </p>
            </div>
            <div class="flex gap-4 justify-between flex-col">
              <WynLabelInput typeInput="email" hintInput="example@mail.ru" nameInput="email" idInput="heroEmail"
                v-model.trim.lazy="formData.email.value">
                Почта
              </WynLabelInput>
              <WynLabelInput typeInput="password" hintInput="Password123!" nameInput="password" idInput="heroPassword"
                v-model.trim.lazy="formData.password.value">
                Пароль
              </WynLabelInput>
            </div>
          </div>
          <WynButton type="submit" typeBtn="solid"
            class="bg-red-400 rounded-full px-11 text-white hover:bg-transparent hover:text-white border-2 border-red-400">
            Начнём!</WynButton>
        </form>
      </div>
      <div class="h-[356]">
        <img class="h-full w-full" src="/images/book_reader.svg" alt="иконка читающего человека" />
      </div>
    </WynContent>
  </WynSection>
</template>

<script setup lang="ts">
import WynSection from "~/components/UI/WynSection.vue"
import WynContent from "~/components/UI/WynContent.vue"
import WynLabelInput from "~/components/UI/WynLabelInput.vue"
import WynButton from "~/components/UI/WynButton.vue"

import { ref } from "vue"
const formData = {
  email: ref(""),
  password: ref(""),
  visiblePass: ref(false),
}
</script>
