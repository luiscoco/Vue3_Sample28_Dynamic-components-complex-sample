<template>
  <div id="app">
    <TabbedNavigation />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import TabbedNavigation from "./TabbedNavigation.vue";

export default defineComponent({
  components: {
    TabbedNavigation,
  },
});
</script>

<style>
#app {
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
}
</style>
