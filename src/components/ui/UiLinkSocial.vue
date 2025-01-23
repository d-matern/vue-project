<script setup lang="ts">
withDefaults(
  defineProps<{
    href: string;
    label?: string;
    variant?: 'desktop' | 'mobile';
  }>(),
  {
    variant: 'desktop',
  },
);
</script>

<template>
  <a class="link body-s-500" :href="href" target="_blank" rel="noopener noreferrer">
    <div class="link-icon" :class="`link-${variant}-icon`">
      <slot name="icon" />
    </div>
    <slot v-if="!label" />
    <template v-else>
      {{ label }}
    </template>
  </a>
</template>

<style scoped>
.link {
  width: 64px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  color: var(--white-color);
}

.link:hover,
.link:active {
  color: var(--neutral-175-color);
}

.link-icon {
  width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 12px;
}

.link-desktop-icon {
  color: var(--white-color);
  background: var(--black-opacity-8);
}
.link:hover .link-desktop-icon,
.link:active .link-desktop-icon {
  color: var(--primary-color);
  background: var(--neutral-15-color);
}

.link-mobile-icon {
  color: var(--primary-color);
  background: var(--primary-15-color);
}
.link:hover .link-mobile-icon,
.link:active .link-mobile-icon {
  color: var(--white-color);
  background: var(--primary-color);
}
</style>
