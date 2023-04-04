<template>
  <div class="flex justify-center">
    <div
      class="max-w-sm min-h-max min-w-full bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
    >
      <AtomImage
        class="rounded-t-lg object-cover max-h-72 w-[100%]"
        :img-src="props.cardImageSrc"
      />
      <div class="p-5">
        <AtomTitle :title-text="props.cardTitle" />
        <AtomText v-if="props.cardContents" :text="props.cardContents" />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import AtomImage from "../atoms/AtomImage.vue";
import AtomTitle from "../atoms/AtomTitle.vue";
import AtomText from "../atoms/AtomText.vue";

interface Props {
  cardTitle: string;
  cardContents?: string;
  cardImageSrc: string;
}
const props = defineProps<Props>();
</script>
