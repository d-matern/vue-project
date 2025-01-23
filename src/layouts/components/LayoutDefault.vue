<script setup lang="ts">
import CarouselSocial from '@/components/CarouselSocial.vue';
import NavBar from '@/components/NavBar.vue';
</script>

<template>
  <header>
    <NavBar>
      <template #title>
        <div style="text-align: center">
          <h1 class="body-l-500">Hot Telecom</h1>
          <p class="body-s-400">support service</p>
        </div>
      </template>
      <template #content>
        <CarouselSocial />
      </template>
    </NavBar>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  width: 100vw;
  max-height: 100vh;
}
</style>
