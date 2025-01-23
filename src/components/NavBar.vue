<script setup lang="ts">
import IconChevronDown from './icons/IconChevronDown.vue';
import UiButtonIcon from './ui/UiButtonIcon.vue';
</script>

<template>
  <nav class="nav">
    <div class="nav-head">
      <span />

      <slot name="title" />

      <div class="nav-actions">
        <slot name="actions" />

        <UiButtonIcon size="m" variant="invert">
          <IconChevronDown :size="20" />
        </UiButtonIcon>
      </div>
    </div>

    <slot name="content" />
  </nav>
</template>

<style scoped>
.nav {
  padding: 8px 12px;
  color: var(--white-color);
  background: var(--primary-color);
}

.nav-head {
  width: 100%;
  display: flex;
  align-items: start;
  justify-content: space-between;
  background: var(--primary-color);
}

.nav-actions {
  display: flex;
  align-items: center;
  gap: 12px;
}
</style>
