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
      d="M12.6666 8H3.33331"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
    <path
      d="M7.99998 12.6667L3.33331 8.00004L7.99998 3.33337"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
  </svg>
</template>
