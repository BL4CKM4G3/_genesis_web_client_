<template>
  <div id="app">
    <main-layout></main-layout>
  </div>
</template>

<script>
import MainLayout from "./core/components/MainLayout";

export default {
  components: {
    MainLayout,
  },
};
</script>
<style lang="scss">
#app {
  height: 100vh;
  width: 100vw;
  margin: 0;
  padding: 0;
}
</style>
