<script setup lang="ts">
import { computed } from 'vue';
import { useRoute } from 'vue-router';
import LayoutDefault from './components/LayoutDefault.vue';

const layouts = {
  default: LayoutDefault,
};
const route = useRoute();

const layoutComponent = computed(() => {
  if (route.meta && 'layout' in route.meta) {
    // eslint-disable-next-line @typescript-eslint/ban-ts-comment
    // @ts-ignore
    return layouts[route.meta.layout];
  }
  return layouts.default;
});
</script>

<template>
  <component :is="layoutComponent" />
</template>
