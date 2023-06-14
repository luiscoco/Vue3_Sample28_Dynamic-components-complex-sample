<template>
  <div>
    <div class="tabs">
      <div v-for="(tab, index) in tabs" :key="index" @click="selectTab(tab)">
        {{ tab.name }}
      </div>
    </div>

    <component :is="currentTab.component" v-if="currentTab"></component>
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";

// Import the components for each tab
import Tab1Component from "./Tab1Component.vue";
import Tab2Component from "./Tab2Component.vue";
import Tab3Component from "./Tab3Component.vue";

// Define the tabs
const tabs = ref([
  { name: "Tab 1", component: Tab1Component },
  { name: "Tab 2", component: Tab2Component },
  { name: "Tab 3", component: Tab3Component },
]);

// Define the selected tab
const currentTab = ref(tabs.value[0]);

// Function to select a tab
function selectTab(tab) {
  currentTab.value = tab;
}
</script>
