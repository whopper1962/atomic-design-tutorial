<template>
  <div>
    <OrganismHeader />
    <Home />
    <!-- <router-view></router-view> -->
    <OrganismFooter />
  </div>
</template>

<script setup lang="ts">
import OrganismHeader from "./components/organisms/OrganismHeader.vue";
import OrganismFooter from "./components/organisms/OrganismFooter.vue";
import Home from "./components/templates/TemplateHome.vue";
</script>
