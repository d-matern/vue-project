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
      d="M13.3333 14V12.6667C13.3333 11.9594 13.0524 11.2811 12.5523 10.781C12.0522 10.281 11.3739 10 10.6667 10H5.33332C4.62608 10 3.9478 10.281 3.4477 10.781C2.94761 11.2811 2.66666 11.9594 2.66666 12.6667V14"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
    <path
      d="M8.00001 7.33333C9.47277 7.33333 10.6667 6.13943 10.6667 4.66667C10.6667 3.19391 9.47277 2 8.00001 2C6.52725 2 5.33334 3.19391 5.33334 4.66667C5.33334 6.13943 6.52725 7.33333 8.00001 7.33333Z"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
  </svg>
</template>
