<template>
  <div id="app">
    <!-- <index-page></index-page> -->
    <!-- <router-link to="/login">12312</router-link> -->
    <!-- <login-page></login-page> -->
    <router-link to="/"></router-link>
    <router-view />
  </div>
</template>

<script>
// import Login from './views/Login.vue';
// import Index from './views/Index.vue';

export default {
  name: 'App',
  components: {
    // 'login-page': Login,
    // 'index-page': Index,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  /* margin-top: 60px; */
  height: 100%;
}
</style>
