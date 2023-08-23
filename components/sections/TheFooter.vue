<template>
  <footer class="mt-auto">
    <div class="flex justify-between items-center py-5 px-[5.5rem]">
       <NuxtLink class="h-10" to="/">
        <logo class="!h-full !w-full" filled />
      </NuxtLink>
      <WynNav />
    </div>
    <div class="flex justify-between items-center py-5 px-[5.5rem]">
      <p class="text-gray-600 text-xs font-normal underline"><a href="https://freelance.habr.com/freelancers/Wyndace">© StyleLifeWeb | Васильев Александр, 2023. Копируйте сколько влезет :Р</a></p>
      <ul class="flex gap-2">
        <li class="bg-gray-200 transition-colors duration-300 rounded-md group hover:bg-blue-400 flex items-center justify-center">
          <a class="h-full transition-colors duration-300 w-full p-2 text-gray-600 group-hover:text-white" href="https://vk.com/stylelifeweb.wyndace">
            <vkIcon class="!h-4 !w-4" />
          </a>
        </li>
        <li class="bg-gray-200 transition-colors duration-300 rounded-md group hover:bg-blue-400 flex items-center justify-center">
          <a class="h-full transition-colors duration-300 w-full p-2 inline-block text-gray-600 group-hover:text-white" href="https://tg.me/wyndace">
            <tgIcon class="!h-4 !w-4" />
          </a>
        </li>        
        <li class="bg-gray-200 transition-colors duration-300 rounded-md flex group hover:bg-blue-400 items-center justify-center">
          <a class="h-full w-full transition-colors duration-300 p-2 text-gray-600 group-hover:text-white" href="https://github.com/Wyndace">
            <ghIcon class="!h-4 !w-4" />
          </a>
        </li>
      </ul>
    </div>
  </footer>
</template>


<script setup lang="ts">
import logo from "~/assets/images/icons/Logo.svg"
import WynNav from "~/components/UI/WynNav.vue";
  import vkIcon from "~/assets/images/icons/vk.svg"
  import tgIcon from "~/assets/images/icons/tg.svg"
  import ghIcon from "~/assets/images/icons/github.svg"
</script>
