<script setup lang="ts">
import IconWhatsApp from './icons/IconWhatsApp.vue'
import LinkSocial from './ui/LinkSocial.vue'
</script>

<template>
  <LinkSocial href="" variant="mobile">
    <template #icon>
      <IconWhatsApp />
    </template>
    WhatsApp
  </LinkSocial>
</template>
