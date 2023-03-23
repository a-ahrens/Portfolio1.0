<template>
  <div id="app">
    <nav>
      <h1>ANTHONY AHRENS CODING</h1>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/experience">Experience</router-link> |
      <router-link to="/contact">Contact</router-link>
    </nav>
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: monospace, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #EDF1D6;
  background-color: #609966;
  border: 3px solid lawn;
}

nav {
  padding: 30px;
  background-color: #40513B;
  border-bottom: 3px solid #9DC08B;
}

nav a {
  font-weight: bold;
  color: lawngreen;
}

nav h1 {
  font-size: 48px;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
