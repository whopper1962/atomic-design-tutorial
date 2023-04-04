<template>
  <header>
    <nav class="bg-white border-gray-200 px-4 lg:px-6 py-2.5 dark:bg-gray-800">
      <div
        class="flex flex-wrap justify-between items-center mx-auto max-w-screen-xl"
      >
        <MoleculeHeaderTitleVue />
        <div class="flex items-center lg:order-2">
          <AtomButton
            btn-text="Login"
            :btn-disabled="false"
            :btn-size="`small`"
            @click="login()"
          />
          <AtomButton
            btn-text="SignUp"
            :btn-disabled="false"
            :btn-size="`small`"
            @click="signUp()"
          />
        </div>
        <div
          class="hidden justify-between items-center w-full lg:flex lg:w-auto lg:order-1"
        >
          <MoleculeHeaderLinks />
        </div>
      </div>
    </nav>
  </header>
</template>

<script setup lang="ts">
import AtomButton from "../atoms/AtomButton.vue";
import MoleculeHeaderLinks from "../molecules/MoleculeHeaderLinks.vue";
import MoleculeHeaderTitleVue from "../molecules/MoleculeHeaderTitle.vue";

const login = () => {
  console.log("Login");
};

const signUp = () => {
  console.log("SignUp!");
};
</script>
