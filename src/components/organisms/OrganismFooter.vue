<template>
  <footer class="bg-neutral-200 text-center dark:bg-neutral-700 lg:text-left">
    <div
      class="p-4 text-center text-neutral-700 dark:text-neutral-200 whitespace-nowrap"
    >
      <AtomText :text="`created in 2023:`" />
      <AtomLink
        link-href="https://github.com/whopper1962"
        link-text="Visit whopper1962 github"
      />
    </div>
  </footer>
</template>

<script setup lang="ts">
import AtomLink from "../atoms/AtomLink.vue";
import AtomText from "../atoms/AtomText.vue";
</script>
