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
    <path d="M12 4L4 12" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" />
    <path d="M4 4L12 12" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" />
  </svg>
</template>
