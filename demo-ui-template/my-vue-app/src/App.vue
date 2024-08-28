<template>
  <div id="app">
    <HeaderComponent />
    <div class="tabs">
      <div class="tab-buttons">
        <button v-for="tab in tabs" :key="tab" @click="currentTab = tab" :class="{ active: currentTab === tab }">
          {{ tab }}
        </button>
      </div>
    </div>
    <component :is="currentTabComponent" class="tab-content"></component>
    <FooterComponent />
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';

import HeaderComponent from './components/HeaderComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import HomeTab from './components/HomeTab.vue';
import AboutTab from './components/AboutTab.vue';
import ContactTab from './components/ContactTab.vue';
import WelcomeTab from './components/WelcomeTab.vue';
import ServicesTab from './components/ServicesTab.vue';
import HoursTab from './components/HoursTab.vue';

const tabs = ['Home', 'About', 'Contact', 'Welcome', 'Services', 'Hours'];
const currentTab = ref('Home');

const currentTabComponent = computed(() => {
  switch (currentTab.value) {
    case 'Home':
      return HomeTab;
    case 'About':
      return AboutTab;
    case 'Contact':
      return ContactTab;
    case 'Welcome':
      return WelcomeTab;
    case 'Services':
      return ServicesTab;
    case 'Hours':
      return HoursTab;
    default:
      return HomeTab;
  }
});
</script>

<style scoped>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

main {
  flex: 1;
}

.tabs {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 20px 0;
  background-color: #ffcc00; /* Gold background */
  padding: 20px;
  border-radius: 8px;
}

.tabs img {
  margin-bottom: 10px;
}

.tab-buttons {
  display: flex;
}

.tab-buttons button {
  padding: 10px 20px;
  margin: 0 5px;
  cursor: pointer;
  border: 2px solid #b22222; /* Dark red border */
  background-color: #ffcc00; /* Gold background */
  color: #b22222; /* Dark red text */
  font-size: 16px;
  border-radius: 5px;
  transition: background-color 0.3s, color 0.3s;
}

.tab-buttons button.active {
  background-color: #b22222; /* Dark red background */
  color: white; /* White text */
}

.tab-content {
  padding: 20px;
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}
</style>
