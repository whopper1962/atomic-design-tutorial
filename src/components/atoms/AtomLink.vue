<template>
  <a
    :href="props.linkHref"
    class="text-neutral-800 dark:text-neutral-400"
    :class="props.class"
  >
    <template v-if="props.linkText">{{ props.linkText }}</template>
    <slot />
  </a>
</template>

<script setup lang="ts">
interface Props {
  class?: string;
  linkHref: string;
  linkText?: string;
}
const props = defineProps<Props>();
</script>
