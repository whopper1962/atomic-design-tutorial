<template>
  <img :src="props.imgSrc" :alt="props.imgAlt" :class="props.class" />
</template>

<script setup lang="ts">
interface Props {
  class: string;
  imgSrc: string;
  imgAlt?: string;
}
const props = defineProps<Props>();
</script>
