<template>
  <div class="main-container">
    <div class="spots">
      <div class="border">
        hello
      </div>
      <div class="border">
        world
      </div>
      <div class="border">
        these
      </div>
      <div class="border">
        are
      </div>
      <div class="border">
        your
      </div>
      <div class="border">
        favourite
      </div>
      <div class="border">
        surf
      </div>
      <div class="border">
        spots!
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
}
.spots {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  max-width: 80vw;
  height: 100vh;
  
  background: lightgreen;
}

.border {
  border: solid rgb(51, 66, 131) 2px;
  height: 25vh;
  width: 25vw;
  /* margin: 10px */
}
</style>