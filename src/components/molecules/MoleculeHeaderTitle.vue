<template>
  <AtomLink
    link-href="https://github.com/whopper1962"
    class="flex items-center"
  >
    <AtomImage
      :img-src="`/src/assets/cat.png`"
      :class="`mr-3 h-6 sm:h-9`"
      img-alt="App logo"
    />
    <span
      class="self-center text-xl font-semibold whitespace-nowrap dark:text-white"
    >
      Whopper1962' memes
    </span>
  </AtomLink>
</template>

<script setup lang="ts">
import AtomImage from "../atoms/AtomImage.vue";
import AtomLink from "../atoms/AtomLink.vue";
</script>
