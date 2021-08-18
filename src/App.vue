<template>
  <div id="app">
    <!-- <app-header /> -->
    <router-view/>
    <!-- <app-footer /> -->
  </div>
</template>

<script>
// @ is an alias to /src
// import AppHeader from '@/components/AppHeader.vue'
// import AppFooter from '@/components/AppFooter.vue'

export default {
  components: {
    // AppHeader,
    // AppFooter
  }
}
</script>


<style>

@import url('https://fonts.googleapis.com/css2?family=Poppins&family=Roboto&display=swap');

body {
  margin: 0;
  padding: 0;
  height: 100vh;
}

#app {
  font-family: 'Poppins', 'Roboto', Avenir, Helvetica, Arial, sans-serif;
  color: rgb(58, 58, 58);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
