<script setup lang="ts">
import { computed, ref } from 'vue';
import IconChevronLeft from './icons/IconChevronLeft.vue';
import IconChevronRight from './icons/IconChevronRight.vue';
import IconTelegram from './icons/IconTelegram.vue';
import IconViber from './icons/IconViber.vue';
import IconWechat from './icons/IconWechat.vue';
import IconWhatsApp from './icons/IconWhatsApp.vue';
import UiButtonIcon from './ui/UiButtonIcon.vue';
import UiLinkSocial from './ui/UiLinkSocial.vue';

const socialLinks = [
  {
    label: 'WhatsApp',
    href: '',
    svgComponent: IconWhatsApp,
  },
  {
    label: 'Telegram',
    href: '',
    svgComponent: IconTelegram,
  },
  {
    label: 'WeChat',
    href: '',
    svgComponent: IconWechat,
  },
  {
    label: 'Viber',
    href: '',
    svgComponent: IconViber,
  },
];

const carouselTrackRef = ref<HTMLUListElement | null>(null);

const elementWidth = computed(() => {
  if (carouselTrackRef.value) {
    return carouselTrackRef.value.scrollWidth / socialLinks.length;
  }
  return 0;
});

const prevItem = () => {
  if (carouselTrackRef.value && elementWidth.value) {
    carouselTrackRef.value.scrollLeft = carouselTrackRef.value.scrollLeft - elementWidth.value;
  }
};
const nextItem = () => {
  if (carouselTrackRef.value && elementWidth.value) {
    carouselTrackRef.value.scrollLeft = carouselTrackRef.value.scrollLeft + elementWidth.value;
  }
};
</script>

<template>
  <div class="carousel">
    <UiButtonIcon variant="invert" @click="prevItem">
      <IconChevronLeft />
    </UiButtonIcon>

    <ul ref="carouselTrackRef" class="carousel-track">
      <li v-for="item of socialLinks" :key="item.label">
        <UiLinkSocial :href="item.href">
          <template #icon>
            <component :is="item.svgComponent" />
          </template>
          {{ item.label }}
        </UiLinkSocial>
      </li>
    </ul>

    <UiButtonIcon variant="invert" @click="nextItem">
      <IconChevronRight />
    </UiButtonIcon>
  </div>
</template>

<style scoped>
.carousel {
  width: 100%;
  margin-top: 16px;

  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 8px;

  overflow: hidden;
}

.carousel-track {
  width: 100%;

  display: grid;
  grid-auto-flow: column;
  grid-gap: 4px;

  overflow-x: auto;
  overflow-y: hidden;
  overscroll-behavior-x: contain;
  scroll-snap-type: x mandatory;
  scroll-behavior: smooth;

  list-style: none;

  -ms-overflow-style: none;
  scrollbar-width: none;
}

.carousel-track a {
  scroll-snap-align: start;
}
</style>
