<script setup lang="ts">
withDefaults(
  defineProps<{
    size?: number
  }>(),
  {
    size: 16,
  },
)
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
      d="M5 12C4.44772 12 4 11.5523 4 11V5C4 4.44772 4.44772 4 5 4H11C11.5523 4 12 4.44772 12 5V11C12 11.5523 11.5523 12 11 12H5Z"
      fill="black"
    />
  </svg>
</template>
