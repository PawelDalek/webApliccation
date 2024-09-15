<template>
  <div class="app">
    <Sidebar />
    <main>
      <router-view />
    </main>
  </div>
</template>

<script setup>
import Sidebar from './components/Sidebar.vue';
</script>

<style lang="scss">
:root {
  --primary: #f5f5f5b4;
  --blue: #0055ffb4;
  --ashen: #e2b6b6b4;
  --light: #dff0e2;
  --sidebar-width: 300px;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Fira sans', sans-serif;
}

body {
  background: var(--light);
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

main {
  flex: 1 1 0;
  padding: 2rem;
  margin-left: var(--sidebar-width);
}

@media (max-width: 768px) {
  main {
    padding-left: 4rem;
  }
}}
</style>