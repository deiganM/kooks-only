<template>
  <div class="home">
    <h1>Choose your local surf spot</h1>
    <surf-spots />
  </div>
</template>

<script>
// @ is an alias to /src
import SurfSpots from '../components/SurfSpots.vue'

export default {
  name: 'Home',
  components: {
    SurfSpots
  }
}
</script>

<style scoped>
.home {
  height: 100vh;
}
</style>
