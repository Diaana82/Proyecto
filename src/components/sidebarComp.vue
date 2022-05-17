<template>
 <aside :class="`${isExpanded && 'isExpanded'}`">
    <div class="logo">
      <img src="../assets/sidebar/logoo.png" alt="Logo">
    </div>

    <div class="menu-toggle-wrap">
      <button class="menu-toggle" @click="toggleMenu">
        <img class="material-icons" src="../assets/sidebar/button.png" alt="double">
      </button>
    </div>
  </aside>
</template>

<script>
import { ref } from 'vue'
const isExpanded = ref(false)

export default {
  name: 'sidebarComp',
  methods: {
    toggleMenu: () => {
      isExpanded.value = !isExpanded.value
    }
  }
}
</script>

<style scoped>
aside {
  display: flex;
  flex-direction: column;
  width: calc(2rem + 32px);
  min-height: 100vh;
  overflow: hidden;
  padding: 1rem;

  background-color: var(--primary-color);
  color: var(--light);
  transition: 0.2s ease-out;

  @media (max-width: 768px) {
    position: fixed;
    z-index: 99;
    }
}

.logo{
  margin: 1rem,
}
img {
  width: 2rem;
}

</style>
