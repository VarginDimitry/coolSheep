<script setup lang="ts">
import { computed } from 'vue'
const props = defineProps<{
  isActive: boolean
}>()
const fileName = computed(() => (props.isActive ? 'pistones_active.png' : 'pistones_disabled.png'))
</script>

<template>
  <div class="piston-component">
    <img :src="`/coolSheep/${fileName}`" />
  </div>
</template>

<style scoped>
.piston-component {
  width: 100px;
  height: 170px;
}
.piston-component img {
  width: 100%;
  height: 100%;
  display: flex;
  transform: rotate(242deg);
}
</style>
