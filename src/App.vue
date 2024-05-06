<template>
  <header>
    <div class="logo-wrapper">
      <img alt="Vue logo" class="logo" src="@/assets/Monyet.png" width="220" height="220" />
      <HelloWorld msg="Reza Ibnu Hanifa" />
    </div>

    <nav>
  
    </nav>
  </header>

  <RouterView />
</template>

<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
</script>

<style>
header {
 
  background-color: transparent;
  padding: 20px;
}

.logo-wrapper {
  display: flex;
  align-items: center;
  margin-bottom: 20px;
}

.logo {
  margin-right: 20px;
}

nav {
  display: flex;
  justify-content: center;
}

nav a {
  text-decoration: none;
  color: #333;
  padding: 10px 20px;
  border-radius: 5px;
  margin: 0 10px;
  transition: background-color 0.3s ease;
}

nav a:hover {
  background-color: #ddd;
}

@media (min-width: 1024px) {
  .logo-wrapper {
    margin-bottom: 0;
  }

  nav {
    margin-top: 0;
  }
}
</style>
