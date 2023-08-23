<template>
  <div class="flex gap-2 w-full flex-col">
    <label :for="idInput" class="block mb-1 text-base font-medium text-white">
      <slot />
    </label>
    <div class="relative">
      <div class="absolute inset-y-0 left-0 flex items-center justify-between pl-4 pointer-events-none">
        <EmailIcon class="!h-6 !w-6 text-white" v-if="typeInput === 'email'" />
        <PasswordIcon class="!h-6 !w-6 text-white" v-if="typeInput === 'password'" />
      </div>
      <input :type="typeInput" :name="nameInput" :id="idInput" :value="modelValue" @input="updateInput"
        class="w-full bg-transparent text-white placeholder:text-gray-200 p-4 pl-12 border-white border rounded-md text-base font-normal"
        :placeholder="hintInput" />
    </div>
  </div>
</template>

<script lang="ts" setup>
import EmailIcon from "~/assets/images/icons/email.svg"
import PasswordIcon from "~/assets/images/icons/Password.svg"
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
  emit("update:modelValue", e?.target.value)
}
</script>
