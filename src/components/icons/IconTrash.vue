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
      d="M2 4H3.33333H14"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
    <path
      d="M12.6666 4.00004V13.3334C12.6666 13.687 12.5262 14.0261 12.2761 14.2762C12.0261 14.5262 11.6869 14.6667 11.3333 14.6667H4.66665C4.31302 14.6667 3.97389 14.5262 3.72384 14.2762C3.47379 14.0261 3.33331 13.687 3.33331 13.3334V4.00004M5.33331 4.00004V2.66671C5.33331 2.31309 5.47379 1.97395 5.72384 1.7239C5.97389 1.47385 6.31302 1.33337 6.66665 1.33337H9.33331C9.68693 1.33337 10.0261 1.47385 10.2761 1.7239C10.5262 1.97395 10.6666 2.31309 10.6666 2.66671V4.00004"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
  </svg>
</template>
