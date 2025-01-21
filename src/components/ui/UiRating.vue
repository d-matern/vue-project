<script setup lang="ts">
import { ref, watch } from 'vue';
import IconRating from '../icons/IconRating.vue';

const MAX_RATING_STAR = 5;

const props = withDefaults(
  defineProps<{
    rating?: number;
  }>(),
  {
    rating: 0,
  },
);
const emit = defineEmits(['update:rating']);

const internalRating = ref(0);

const handleChange = (count: number) => {
  internalRating.value = count;
  emit('update:rating', internalRating.value);
};

const handleHover = (count: number) => {
  internalRating.value = count;
};

watch(
  () => props.rating,
  (value) => {
    if (typeof value === 'number') {
      internalRating.value = value;
    }
  },
  { immediate: true },
);
</script>

<template>
  <div class="container">
    <IconRating
      v-for="starIndex of MAX_RATING_STAR"
      :key="starIndex"
      class="rating"
      :class="internalRating >= starIndex ? 'rating-active' : 'rating'"
      @click="handleChange(starIndex)"
      @mouseenter="handleHover(starIndex)"
      @mouseleave="handleHover(rating)"
    />
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 4;
}

.rating {
  color: var(--neutral-color);
  cursor: pointer;
}

.rating-active,
.rating:active,
.rating:hover {
  color: var(--primary-color);
}
</style>
