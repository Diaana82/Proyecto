<template>
  <div class="app">
    <sidebarComp />
    <router-view/>
  </div>
</template>

<script setup>
import sidebarComp from '@/components/sidebarComp.vue'
</script>

<style>
:root {
  --primary-color: #FFB74A;
  --orange: #FFB74A9C;
  --Brown: #9D6342;
  --dark: #000000;
  --sidebar-whdth: 300px;
  }
* {
  margin:0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Fira sans', sans-serif;
  }
  body {
    background: white;
  }
  button {
    cursor: pointer;
    appearance: none;
    border: none;
    outline: none;
    background: none;
  }
  .app {
    display: flex;
  }
</style>
