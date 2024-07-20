<script setup lang="ts">
defineProps<{
  isActive: boolean
}>()
</script>

<template>
  <div class="end-rod-component">
    <img src="/coolSheep/end_rod.png" />
  </div>
</template>

<style scoped>
.end-rod-component {
  width: 100px;
  height: 100px;
}
.end-rod-component img {
  width: 100%;
  height: 100%;
  display: block;
  transform: rotate(335deg);
}
</style>
