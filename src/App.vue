<template>
  <!-- #app is how we load our App.vue file trough main.js -->
  <div id="app">
    <!-- we are not allowed to remove router-view -->
    <router-view/>
  </div>
</template>



<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body {
  margin: 0;
}
</style>
