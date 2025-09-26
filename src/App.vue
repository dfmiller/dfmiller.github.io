<script setup lang="ts">
import { ref } from 'vue';
import { RouterLink, RouterView } from 'vue-router'
import PageHeader from './components/PageHeader.vue'

const isActive = ref(false);

const toggleNav = () => {
  isActive.value = !isActive.value;
}

</script>

<template>
  <PageHeader @toggle-nav="toggleNav" />

  <RouterView />

  <nav :class="['nav', { active: isActive } ]">
    <RouterLink to="/">Home</RouterLink>
    <RouterLink to="/about">About</RouterLink>
  </nav>
</template>

<style scoped>

nav {
  background: linear-gradient(45deg, azure, lightblue);;
  width: 100%;
  max-height: 100%;
  box-sizing: border-box; 
  padding: 24px;
  position: sticky; 
  left: 0;
  bottom: -100%;
  z-index: 700;
  overflow: auto;
  border-radius: 8px 8px 0 0;
  transition: .25s bottom;
	
   li {
    list-style: none; 
    padding: 16px;
    margin:0;
   }
	
   &.active {
    bottom: 0;
   }
 }

</style>