<script setup lang="ts">
import { ref } from 'vue'

const items = ref([
  {
    src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg'
  },
  {
    src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg'
  },
  {
    src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg'
  },
  {
    src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg'
  }
])
</script>

<template>
  <v-carousel :show-arrows="true">
    <v-carousel-item v-for="(item, i) in items" :key="i" :src="item.src" cover></v-carousel-item>
  </v-carousel>
</template>
