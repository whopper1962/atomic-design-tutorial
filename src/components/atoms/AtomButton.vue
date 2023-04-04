<template>
  <button
    class="text-white min-w-fit bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:ring-blue-300 font-medium rounded-lg text-sm px-4 lg:px-5 py-2 lg:py-2.5 mr-2 dark:bg-blue-600 dark:hover:bg-blue-700 focus:outline-none dark:focus:ring-blue-800"
    :disabled="props.btnDisabled"
    :class="{
      'w-96': props.btnSize === BtnSize.LARGE,
      'w-64': props.btnSize === BtnSize.MEDIUM,
      'w-32': props.btnSize === BtnSize.SMALL,
    }"
    @click="onClickButton()"
  >
    {{ props.btnText }}
  </button>
</template>

<script setup lang="ts">
const BtnSize = {
  LARGE: "large",
  MEDIUM: "medium",
  SMALL: "small",
} as const;
type BtnSize = typeof BtnSize[keyof typeof BtnSize];

interface Props {
  btnText?: string;
  btnDisabled: boolean;
  btnSize: BtnSize;
  class?: string;
}

const props = defineProps<Props>();

const emit = defineEmits<{
  (e: "click"): void;
}>();

const onClickButton = (): void => {
  emit("click");
};
</script>
