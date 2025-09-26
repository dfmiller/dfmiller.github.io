<script setup lang="ts">

const emit = defineEmits(['toggle-nav']);

const toggleNav = () => {
  emit('toggle-nav');
}

</script>

<template>
  <header class="page-header">
    Night 828
    <i class="ph-bold ph-list" @click="toggleNav"></i>
  </header>
</template>

<style scoped>

header {
  display: flex;
  justify-content: space-between; 
  align-items: center;
  background: linear-gradient(45deg, azure, lightblue);
  height: 64px;
  padding: 16px;
  box-sizing: border-box;
  position: sticky; 
  top: 0;
  left: 0;
  right: 0;
  width: 100vw;
  z-index: 600;
  font-size: 24px;
  a {
   color: inherit;
   text-decoration: none;
  }
 }

</style>
