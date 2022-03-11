<template>
  <nav>
    <router-link :to="{ name: 'Activities' }">Activities</router-link>
  </nav>
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: navy;
}

nav {
  padding: 30px;
}

nav a {
  font-size: 48px;  
  font-weight: bold;
  color: navy;
  text-decoration: none;
  padding: 10px;
  border-radius: 4px;
}

nav a.router-link-exact-active {
  color: white;
  background: navy;
}
</style>
