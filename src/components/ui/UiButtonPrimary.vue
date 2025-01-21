<script setup lang="ts">
withDefaults(
  defineProps<{
    size?: 's' | 'm' | 'l';
    variant?: 'primary' | 'invert' | 'attention';
    isDisabled?: boolean;
  }>(),
  {
    size: 's',
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
  width: fit-content;
  display: flex;
  align-items: center;
  justify-content: center;

  font-family: 'Hind-SemiBold';
  text-transform: uppercase;
}

.button-size-s {
  height: 32px;
  padding: 0 8px;
  border-radius: 10px;
  font-size: 14px;
  line-height: 19.6px;
}

.button-size-m {
  height: 40px;
  padding: 0 12px;
  border-radius: 12px;
  font-family: 'Hind-Medium';
  font-size: 16px;
  line-height: 22.4px;
}

.button-size-l {
  height: 44px;
  padding: 0 16px;
  border-radius: 16px;
  font-size: 16px;
  line-height: 22.4px;
}

.button-variant-primary {
  color: var(--white-color);
  border: 1px solid var(--primary-color);
  background: var(--primary-color);
}
.button-variant-primary:hover {
  border-color: var(--primary-125-color);
  background: var(--primary-125-color);
}
.button-variant-primary:disabled {
  color: var(--white-color);
  border-color: var(--primary-75-color);
  background: var(--primary-75-color);
}
.button-variant-primary:active {
  border-color: var(--primary-125-color);
  background: var(--primary-color);
}

.button-variant-invert {
  color: var(--primary-color);
  border: 1px solid var(--primary-color);
  background: var(--white-color);
}
.button-variant-invert:hover {
  background: var(--primary-15-color);
}
.button-variant-invert:disabled {
  color: var(--primary-75-color);
  border-color: var(--white-color);
}
.button-variant-invert:active {
  border-width: 2px;
  background: var(--white-color);
  transition: transform 0s;
}

.button-variant-attention {
  color: var(--error-125-color);
  border: 1px solid var(--error-50-color);
  background: var(--error-50-color);
}
.button-variant-attention:hover {
  border-color: var(--error-25-color);
  background: var(--error-25-color);
}
.button-variant-attention:disabled {
  border-color: var(--error-5-color);
  background: var(--error-5-color);
}
.button-variant-attention:active {
  border-color: var(--error-125-color);
  background: var(--error-50-color);
}
</style>
