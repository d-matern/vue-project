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
      d="M7.99998 8.66671C8.36817 8.66671 8.66665 8.36823 8.66665 8.00004C8.66665 7.63185 8.36817 7.33337 7.99998 7.33337C7.63179 7.33337 7.33331 7.63185 7.33331 8.00004C7.33331 8.36823 7.63179 8.66671 7.99998 8.66671Z"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
    <path
      d="M7.99998 3.99996C8.36817 3.99996 8.66665 3.70148 8.66665 3.33329C8.66665 2.9651 8.36817 2.66663 7.99998 2.66663C7.63179 2.66663 7.33331 2.9651 7.33331 3.33329C7.33331 3.70148 7.63179 3.99996 7.99998 3.99996Z"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
    <path
      d="M7.99998 13.3333C8.36817 13.3333 8.66665 13.0349 8.66665 12.6667C8.66665 12.2985 8.36817 12 7.99998 12C7.63179 12 7.33331 12.2985 7.33331 12.6667C7.33331 13.0349 7.63179 13.3333 7.99998 13.3333Z"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
  </svg>
</template>
