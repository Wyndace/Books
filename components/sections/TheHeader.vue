<template>
  <header class="py-5 px-[5.5rem] flex items-center justify-between mb-5">
      <NuxtLink class="h-10" to="/">
        <logo class="!h-full !w-full" filled />
      </NuxtLink>
      <WynNav />
     <div class="flex items-center gap-5">
       <WynButton type-btn="outline" class="px-4 rounded-full text-xs font-medium">Зарегистрироваться</WynButton>
       <WynButton type-btn="solid" class="px-11 rounded-full text-xs font-medium">Войти</WynButton>
     </div> 
  </header>
</template>

<script setup lang="ts">
  import logo from "~/assets/images/icons/Logo.svg";
  import WynButton from "~/components/UI/WynButton.vue";
  import WynNav from "~/components/UI/WynNav.vue";
</script>
