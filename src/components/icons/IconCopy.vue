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
    <g clip-path="url(#clip0_514_20401)">
      <path
        d="M13.3333 6H7.33333C6.59695 6 6 6.59695 6 7.33333V13.3333C6 14.0697 6.59695 14.6667 7.33333 14.6667H13.3333C14.0697 14.6667 14.6667 14.0697 14.6667 13.3333V7.33333C14.6667 6.59695 14.0697 6 13.3333 6Z"
        stroke="currentColor"
        stroke-linecap="round"
        stroke-linejoin="round"
      />
      <path
        d="M3.33331 10H2.66665C2.31302 10 1.97389 9.85956 1.72384 9.60952C1.47379 9.35947 1.33331 9.02033 1.33331 8.66671V2.66671C1.33331 2.31309 1.47379 1.97395 1.72384 1.7239C1.97389 1.47385 2.31302 1.33337 2.66665 1.33337H8.66665C9.02027 1.33337 9.35941 1.47385 9.60946 1.7239C9.8595 1.97395 9.99998 2.31309 9.99998 2.66671V3.33337"
        stroke="currentColor"
        stroke-linecap="round"
        stroke-linejoin="round"
      />
    </g>
    <defs>
      <clipPath id="clip0_514_20401">
        <rect width="16" height="16" fill="white" />
      </clipPath>
    </defs>
  </svg>
</template>
