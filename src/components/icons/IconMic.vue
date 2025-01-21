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
      d="M8 0.67C7.46957 0.67 6.96086 0.880638 6.58579 1.25558C6.21071 1.63052 6 2.13904 6 2.66929V8.00071C6 8.53096 6.21071 9.03948 6.58579 9.41442C6.96086 9.78936 7.46957 10 8 10C8.53043 10 9.03914 9.78936 9.41421 9.41442C9.78929 9.03948 10 8.53096 10 8.00071V2.66929C10 2.13904 9.78929 1.63052 9.41421 1.25558C9.03914 0.880638 8.53043 0.67 8 0.67Z"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
    <path
      d="M12.6684 6.5V7.83333C12.6684 9.07101 12.1769 10.258 11.3021 11.1332C10.4272 12.0083 9.24064 12.5 8.0034 12.5C6.76617 12.5 5.57961 12.0083 4.70475 11.1332C3.82989 10.258 3.3384 9.07101 3.3384 7.83333V6.5"
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
      d="M5.33334 15.3334H10.6667"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
  </svg>
</template>
