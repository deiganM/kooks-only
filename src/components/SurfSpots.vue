<template>
  <div class="main-container">
    <div class="surf-spot-container">
      <div class="location-container">
        <p>Long Beach</p>
      </div>
      <div class="location-container">
        <p>Chesterman Beach (North)</p>
      </div>
      <div class="location-container">
        <p>Chesterman Beach (South)</p>
      </div>
      <div class="location-container">
        <p>Wickaninnish</p>
      </div>
      <div class="location-container">
        <p>Cox Bay</p>
      </div>
      <div class="location-container">
        <p>Sombrio</p>
      </div>
      <div class="location-container">
        <p>Jordan River</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.main-container {
  display: flex;
  justify-content: center;
  /* height: 100vh; */
}
.surf-spot-container {
  display: flex;
  flex-wrap: wrap;
  justify-content:center;
  width: 80vw;
  /* height: 100%; */
  padding: 2rem 1rem;
  background: lightgreen;
}

.location-container {
  display: flex;
  justify-content: center;
  border: solid rgb(51, 66, 131) 2px;
  height: 200px;
  width: 200px;
  margin: 10px;
}
</style>