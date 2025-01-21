<script setup lang="ts">
import IconChatFill from '../icons/IconChatFill.vue';

withDefaults(
  defineProps<{
    isNotification?: boolean;
  }>(),
  {
    isNotification: false,
  },
);
</script>

<template>
  <button class="button">
    <div v-if="isNotification" class="button-notification" />
    <IconChatFill :size="24" />
  </button>
</template>

<style>
.button {
  min-width: 52px;
  max-width: 52px;
  min-height: 52px;
  max-height: 52px;

  display: flex;
  align-items: center;
  justify-content: center;

  position: fixed;
  right: 16px;
  bottom: 20px;
  z-index: 9999;

  color: var(--white-color);
  border: 1px solid var(--primary-color);
  border-radius: 50%;
  background: var(--primary-color);
}

.button:hover {
  isolation: isolate;
  box-shadow:
    0px 60px 24px rgba(110, 128, 248, 0.03),
    0px 34px 20px rgba(110, 128, 248, 0.07),
    0px 15px 15px rgba(110, 128, 248, 0.13),
    0px 4px 8px rgba(110, 128, 248, 0.15);
}

.button:active {
  border-color: var(--primary-125-color);
}

.button-notification {
  width: 8px;
  height: 8px;

  position: absolute;
  top: 18px;
  left: 30px;

  background: var(--orange-color);
  border-radius: 50%;
}
</style>
