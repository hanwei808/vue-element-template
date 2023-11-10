<template>
  <div class="app-header">
    <div class="left">
      <ToggleSidebar />
      <Breadcrumb />
    </div>
    <div class="right">
      <FullScreen />
      <h1>Header</h1>
    </div>
  </div>
</template>

<script setup lang="ts">
import ToggleSidebar from './ToggleSidebar.vue';
import Breadcrumb from './Breadcrumb.vue'
import FullScreen from './FullScreen.vue'
</script>

<style lang="scss" scoped>
.app-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    .left,.right {
        display: flex;
        align-items: center;
    }
}
</style>