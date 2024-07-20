<script setup lang="ts">
defineProps<{
  isActive: boolean
}>();
</script>

<template>
  <div class="sheep-component">
    <img src="/coolsheep/sheep.png">
  </div>
</template>

<style scoped>
.sheep-component {
  width: 240px;
  height: 160px;
}
.sheep-component img {
  width: 100%;
  height: 100%;
  display: block;
}
</style>
