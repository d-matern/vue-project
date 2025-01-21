<script setup lang="ts">
import { ref } from 'vue';
import UiRating from './ui/UiRating.vue';

const r = ref(3);
</script>

<template>
  <UiRating v-model:rating="r" />
</template>
