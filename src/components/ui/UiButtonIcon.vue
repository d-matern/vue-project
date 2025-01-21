<script setup lang="ts">
withDefaults(
  defineProps<{
    size?: 'xs' | 's' | 'm';
    variant?: 'primary' | 'invert' | 'conservative';
    isDisabled?: boolean;
  }>(),
  {
    size: 'xs',
    variant: 'primary',
    isDisabled: false,
  },
);
</script>

<template>
  <button
    class="button"
    :class="`button-size-${size} button-variant-${variant}`"
    :disabled="isDisabled"
  >
    <slot />
  </button>
</template>

<style scoped>
.button {
  display: flex;
  align-items: center;
  justify-content: center;
  background: transparent;
}

.button-size-xs {
  width: 20px;
  height: 20px;
  border-radius: 6px;
}

.button-size-s {
  width: 24px;
  height: 24px;
  border-radius: 8px;
}

.button-size-m {
  width: 36px;
  height: 36px;
  border-radius: 8px;
}

.button-variant-primary {
  color: var(--primary-color);
}
.button-variant-primary:hover {
  color: var(--primary-125-color);
}
.button-variant-primary:disabled {
  color: var(--primary-75-color);
}
.button-variant-primary:active {
  background: var(--primary-opacity-25);
}

.button-variant-invert {
  color: var(--white-color);
}
.button-variant-invert:hover {
  background: var(--black-opacity-8);
}
.button-variant-invert:disabled {
  color: var(--white-opacity-45);
}
.button-variant-invert:active {
  background: var(--black-opacity-8);
}

.button-variant-conservative {
  color: var(--neutral-175-color);
}
.button-variant-conservative:hover {
  background: var(--black-opacity-8);
}
.button-variant-conservative:disabled {
  color: var(--black-opacity-35);
}
.button-variant-conservative:active {
  background: var(--black-opacity-8);
}
</style>
