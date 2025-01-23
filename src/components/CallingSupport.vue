<script setup lang="ts">
import { onMounted, onUnmounted, ref } from 'vue';
import IconMicOff from './icons/IconMicOff.vue';
import IconPhoneOff from './icons/IconPhoneOff.vue';
import IconVolumeOff from './icons/IconVolumeOff.vue';
import UiButtonIcon from './ui/UiButtonIcon.vue';
import UiButtonPrimary from './ui/UiButtonPrimary.vue';

defineProps<{
  isCalling: boolean;
}>();
const emit = defineEmits(['change:isCalling']);

const intervalId = ref<number>();
const callingTime = ref('00:00');
const isVolumeOff = ref(false);
const isMicOff = ref(false);

const toggleVolume = () => {
  isVolumeOff.value = !isVolumeOff.value;
};

const toggleMic = () => {
  isMicOff.value = !isMicOff.value;
};

const handleEndCall = () => {
  emit('change:isCalling', false);
};

onMounted(() => {
  let seconds = 50;
  let minutes = 59;

  intervalId.value = setInterval(() => {
    seconds++;

    if (seconds > 59) {
      minutes++;
      seconds = 0;
    }
    if (minutes > 59) {
      clearInterval(intervalId.value);
      handleEndCall();
    }
    callingTime.value = `${minutes.toLocaleString().padStart(2, '0')}:${seconds.toLocaleString().padStart(2, '0')}`;
  }, 1000);
});

onUnmounted(() => {
  if (intervalId.value) {
    clearInterval(intervalId.value);
  }
});
</script>

<template>
  <div class="call">
    <div class="call-info">
      <p class="call-info--text body-s-500">Call with assistant</p>
      <span class="call-info--text body-xs-400">{{ callingTime }}</span>
    </div>

    <div class="call-actions">
      <UiButtonIcon size="m" variant="invert" :is-active="isVolumeOff" @click="toggleVolume">
        <IconVolumeOff :size="20" />
      </UiButtonIcon>

      <UiButtonIcon size="m" variant="invert" :is-active="isMicOff" @click="toggleMic">
        <IconMicOff :size="20" />
      </UiButtonIcon>

      <UiButtonPrimary class="call-off-btn" size="s" variant="attention" @click="handleEndCall">
        <IconPhoneOff />
      </UiButtonPrimary>
    </div>
  </div>
</template>

<style scoped>
.call {
  padding: 0 4px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: var(--neutral-color);
}

.call-info {
  display: flex;
  align-items: center;
  gap: 8px;
}

.call-info--text {
  color: var(--white-color);
}

.call-actions {
  display: flex;
  align-items: center;
  gap: 12px;
}

.call-off-btn {
  width: 32px !important;
  padding: 0 !important;
}
</style>
