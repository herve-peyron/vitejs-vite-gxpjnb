<script setup>
import DesktopNavbar from './DesktopNavbar.vue';
import MobileNavbar from './MobileNavbar.vue';
</script>

<template>
  <desktop-navbar class="deskx-navbar"></desktop-navbar>
  <mobile-navbar class="mobx-navbar"></mobile-navbar>
</template>

<style lang="less">
.mobx-navbar {
  background-color: lighten(green, 10%);
}

.deskx-navbar {
  background-color: green;
}
</style>
