<script setup lang="ts">
withDefaults(
  defineProps<{
    size?: number;
  }>(),
  {
    size: 16,
  },
);
</script>

<template>
  <svg
    :width="size"
    :height="size"
    viewBox="0 0 16 16"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
  >
    <path
      d="M8.66669 11.3333L12 7.99996L8.66669 4.66663"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
    <path
      d="M4 11.3333L7.33333 7.99996L4 4.66663"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
  </svg>
</template>
