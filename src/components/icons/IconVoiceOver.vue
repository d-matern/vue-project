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
      d="M7.33331 3.33337L3.99998 6.00004H1.33331V10H3.99998L7.33331 12.6667V3.33337Z"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
    <path
      d="M12.7133 3.28662C13.9631 4.53681 14.6652 6.23219 14.6652 7.99995C14.6652 9.76772 13.9631 11.4631 12.7133 12.7133M10.36 5.63995C10.9849 6.26505 11.3359 7.11274 11.3359 7.99662C11.3359 8.8805 10.9849 9.7282 10.36 10.3533"
      stroke="currentColor"
      stroke-linecap="round"
      stroke-linejoin="round"
    />
  </svg>
</template>
