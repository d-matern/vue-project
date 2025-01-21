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
      d="M10 12L6 8L10 4"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
  </svg>
</template>
