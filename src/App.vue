<template>
  <v-app>
    <Sidebar @selectOption="onSelectOption" />
    <v-main>
      <ImageGallery :isWithColor="isWithColor" />
    </v-main>
  </v-app>
</template>

<script setup>
import ImageGallery from "./components/ImageGallery.vue";
import Sidebar from "./components/Sidebar.vue";
import { ref } from "vue";

const isWithColor = ref(true);

const onSelectOption = (isColor) => {
  isWithColor.value = isColor;
};
</script>
