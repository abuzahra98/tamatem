<template>
  <v-main class="main-container">
    <router-view />
  </v-main>
</template>

<script lang="ts" setup>
  //
</script>
<style scoped lang="scss">
@import '../../styles/settings.scss';

.main-container {
  background-color: $primary;
  height: 100vh;
}
</style>