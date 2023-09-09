<template>
  <div class="app">
    <header class="navbar">
      <img alt="My image" class="logo" src="image.jpeg" width="100" height="100" />

      <nav class="nav-links">
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
        <router-link to="/resume">Resume</router-link>
        <router-link to="/contact">Contact</router-link>
      </nav>
    </header>

    <main class="page-content">
      <router-view />
    </main>
  </div>
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router';
</script>

<style scoped>
.app {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
}

.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: navy;
  color: white;
  padding: 0rem;
  width: 100%;
}

.logo {
  width: 125px;
  height: 125px;
  margin: 0 auto 1rem; /* Reduce the margin to create a shorter navbar */
}

.nav-links {
  display: flex;
  justify-content: center;
  align-items: center;
}

.nav-links a {
  color: white;
  text-decoration: none;
  padding: 0.5rem 1rem;
  margin: 0 0.5rem; /* Add margin between links */
}

.nav-links a:hover {
  background-color: rgb(4, 4, 175);
  border-radius: 0.25rem;
  transition: background-color 0.3s;
  color: white;
}

.page-content {
  width: 100%;
  padding: 1rem;
  margin-top: 4rem; /* Add margin to push content below the fixed navbar */
}

@media (min-width: 2000px) {
  .app {
    flex-direction: row;
  }

  .navbar {
    flex-direction: row;
    justify-content: space-between;
    padding: 1rem 2rem;
  }

  .logo {
    margin: 0;
  }

  .nav-links {
    margin-left: 2rem; /* Add margin to separate links from the image */
  }

  .nav-links a {
    margin: 0 1rem; /* Add margin between links */
  }

  .page-content {
    flex-grow: 1;
    margin-top: 4rem; /* Match the margin-top value of .page-content */
  }
}
</style>
