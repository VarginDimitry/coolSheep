<script setup lang="ts">
import { ref, watch } from 'vue'
import MainComponent from './components/MainComponent.vue'

const isActive = ref(false)

watch(isActive, (newValue: boolean) => {
  if (newValue) {
    const pistonAudio = new Audio('/coolSheep/piston_extend.ogg')
    pistonAudio.play()
  } else {
    const pistonAudio = new Audio('/coolSheep/piston_less.ogg')
    pistonAudio.play()
  }
  if (newValue) {
    const sheepAudio = new Audio('/coolSheep/sheep.mp3')
    sheepAudio.play()
  }
})
</script>

<template>
  <div class="main" :class="{ active: isActive }" @click="isActive = !isActive">
    <MainComponent :isActive="isActive" />
  </div>
</template>

<style scoped>
.main {
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #3d7de3de;
}
.active {
  background-color: #e33d50de;
}
</style>
