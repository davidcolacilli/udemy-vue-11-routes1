<template>
  <div id="app" class="container">
    <div id="nav" class="nav">
      <router-link class="nav-item" to="/">Home</router-link>
      <router-link class="nav-item" to="/products">Products</router-link>
      <!-- <router-link class="nav-item" to="/about">About</router-link> -->
      <!-- <router-link class="nav-item" to="/contact">Contact</router-link> -->
      <router-link class="nav-item" to="/users/Juan">Users</router-link>
      <router-link class="nav-item" to="/login">Login</router-link>
      <router-link class="nav-item" to="/signup">Signup</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
}

#nav {
  padding: 2rem 0;
  border-bottom: 1px solid #f0f0f0;
}

#nav a {
  display: inline-block;
  font-weight: bold;
  color: #2c3e50;
  margin: 1rem;
  text-decoration: none;
}

#nav a.router-link-exact-active {
  color: #42b983;
  border-bottom: 2px solid #42b983;
}
</style>
