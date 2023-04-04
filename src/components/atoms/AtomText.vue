<template>
  <p
    class="mb-3 font-normal text-gray-700 dark:text-gray-400"
    :class="{
      'whitespace-nowrap': props.noWrap,
    }"
  >
    {{ props.text }}
  </p>
</template>

<script setup lang="ts">
interface Props {
  text: string;
  noWrap?: boolean;
}
const props = defineProps<Props>();
</script>
