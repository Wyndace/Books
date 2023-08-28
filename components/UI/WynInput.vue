<template>
  <input :type="typeInput" :name="nameInput" :id="idInput" :value="modelValue" @input="updateInput"
    class="w-full bg-transparent text-black placeholder:text-gray-800 p-4 border-white text-base font-normal outline-none"
    :placeholder="hintInput" />
</template>

<script setup lang="ts">
defineProps({
  idInput: {
    type: String,
    required: true,
  },
  nameInput: {
    type: String,
    required: true,
  },
  typeInput: {
    type: String,
    default: "input",
  },
  hintInput: {
    type: String,
    default: "placeholder",
  },
  modelValue: {
    type: String,
    required: true,
  },
})
const emit = defineEmits({
  update: null,
})

function updateInput(e: any) {
  emit("update:modelValue", e.target.value)
}
</script>
