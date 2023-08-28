<template>
  <div>
    <form
      method="POST"
      class="bg-blue-500 py-7 px-5 flex flex-col justify-between rounded-3xl gap-5"
    >
      <div class="flex flex-col justify-between gap-1">
        <WynInput
          typeInput="text"
          hintInput="Введите автора, артикул, название..."
          nameInput="search"
          idInput="search"
          modelValue=""
        >
        </WynInput>
      </div>
      <WynButton
        type="submit"
        typeBtn="solid"
        class="bg-red-400 rounded-full px-11 text-white hover:bg-transparent hover:text-white border-2 border-red-400"
      >
        Начнём!</WynButton
      >
    </form>
  </div>
</template>

<script setup lang="ts"></script>
