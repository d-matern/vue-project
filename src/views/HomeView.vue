<script setup lang="ts">
import CallingSupport from '@/components/CallingSupport.vue';
import { ref } from 'vue';

const isCalling = ref(true);
</script>

<template>
  <main>
    <CallingSupport v-if="isCalling" v-model:is-calling="isCalling" />
  </main>
</template>
