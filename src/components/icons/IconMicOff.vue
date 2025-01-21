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
    <path d="M2 2L14 14" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" />
    <path
      d="M6 6.10577V8.105C6.00035 8.50015 6.11783 8.88634 6.33762 9.21479C6.55741 9.54324 6.86964 9.79921 7.23487 9.95039C7.60011 10.1016 8.00197 10.1411 8.3897 10.0642C8.77743 9.98716 9.13363 9.79703 9.41333 9.51779M10 7.5V2.77372C10.0005 2.27793 9.81669 1.79964 9.48425 1.4317C9.15181 1.06376 8.69447 0.832423 8.201 0.782597C7.70753 0.73277 7.21314 0.86801 6.81381 1.16206C6.41448 1.45611 6.1387 1.88799 6.04 2.37387"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
    <path
      d="M11.1672 11.2456C10.5166 11.9061 9.68246 12.3582 8.77179 12.5439C7.86111 12.7296 6.91542 12.6405 6.05605 12.2878C5.19668 11.9352 4.46282 11.3353 3.94862 10.5649C3.43441 9.79454 3.16332 8.88893 3.17012 7.96426V6.63847M12.5 6.63847V7.96426C12.4998 8.23767 12.4752 8.51051 12.4267 8.77962"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
    <path
      d="M8 12.6666V15.3333"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
    <path
      d="M5.33337 15.3334H10.6667"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
  </svg>
</template>
