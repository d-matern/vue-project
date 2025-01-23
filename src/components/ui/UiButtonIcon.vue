<script setup lang="ts">
withDefaults(
  defineProps<{
    size?: 'xs' | 's' | 'm';
    variant?: 'primary' | 'invert' | 'conservative';
    isActive?: boolean;
    isDisabled?: boolean;
  }>(),
  {
    size: 'xs',
    variant: 'primary',
    isActive: false,
    isDisabled: false,
  },
);
</script>

<template>
  <button
    class="button"
    :class="`
      button-size-${size} button-variant-${variant}
      ${isActive && !isDisabled ? `button-variant-${variant}--active` : ''}
    `"
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
  min-width: 20px;
  min-height: 20px;
  border-radius: 6px;
}

.button-size-s {
  min-width: 24px;
  min-height: 24px;
  border-radius: 8px;
}

.button-size-m {
  min-width: 36px;
  min-height: 36px;
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
.button-variant-primary--active,
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
.button-variant-invert--active,
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
.button-variant-conservative--active,
.button-variant-conservative:active {
  background: var(--black-opacity-8);
}
</style>
