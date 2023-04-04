<template>
  <ul class="flex flex-col mt-4 font-medium lg:flex-row lg:space-x-8 lg:mt-0">
    <li v-for="(link, index) in links" :key="`link_${index}`">
      <AtomLink :link-href="`#`" :link-text="link.text" />
    </li>
  </ul>
</template>

<script setup lang="ts">
import AtomLink from "../atoms/AtomLink.vue";

const links = [
  {
    text: "Memes",
  },
  {
    text: "Categories",
  },
  {
    text: "About us",
  },
];
</script>
