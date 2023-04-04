<template>
  <section class="bg-gray-100 dark:bg-gray-900 py-10 px-12 min-h-[100vh]">
    <div
      class="grid grid-flow-row gap-8 text-neutral-600 sm:grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4"
    >
      <MoleculeCard
        v-for="(meme, index) in memes"
        :key="`card_${index}`"
        :card-image-src="meme.url"
        :card-title="meme.name"
      />
    </div>
  </section>
</template>

<script setup lang="ts">
import axios from "axios";
import { onMounted, ref } from "vue";
import MoleculeCard from "../molecules/MoleculeCard.vue";

let memes = ref<any[]>([]);

onMounted(() => {
  getMemes();
});

const getMemes = async (): Promise<void> => {
  try {
    const { data } = await axios.get(`https://api.imgflip.com/get_memes`);
    memes.value = data.data.memes;
  } catch (err) {
    console.error(err);
    alert(err);
  }
};
</script>
