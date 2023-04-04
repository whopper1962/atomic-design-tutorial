<template>
  <h5
    class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
  >
    {{ props.titleText }}
  </h5>
</template>

<script setup lang="ts">
interface Props {
  titleText: string;
}
const props = defineProps<Props>();
</script>
