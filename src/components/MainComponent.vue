<script setup lang="ts">
import SheepComponent from './SheepComponent.vue'
import PistonComponent from './PistonComponent.vue'
import EndRodComponent from './EndRodComponent.vue'

defineProps<{
  isActive: boolean
}>()
</script>

<template>
  <div class="main-component">
    <SheepComponent class="minecraft sheep" :isActive="isActive" />
    <PistonComponent class="minecraft piston" :isActive="isActive" />
    <EndRodComponent
      class="minecraft end-rod"
      :class="{ 'active-rod': isActive }"
      :isActive="isActive"
    />
  </div>
</template>

<style scoped>
.main-component {
  width: 320px;
  height: 320px;
  margin: auto;
  border: 1px solid black;
}
.minecraft {
  position: relative;
}
.sheep {
  top: 150px;
  right: 20px;
  z-index: 3;
}
.end-rod {
  bottom: 218px;
  left: 135px;
  z-index: 2;
}
.active-rod {
  bottom: 195px;
  left: 90px;
}
.piston {
  bottom: 92px;
  left: 160px;
  z-index: 1;
}
</style>
