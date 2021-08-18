<template>
  <div class="main-container">
    <h1>Choose your surf spot</h1>
    <div class="card-container">
      <div class="surf-spot-container">
        <div class="location-container">
          <h3>{{longBeach.title}}</h3>
          <b>{{longBeach.swell}}</b>
        </div>
        <div class="location-container">
          <h3>{{chestermanN.title}}</h3>
          <b>{{chestermanN.swell}}</b>
        </div>
        <div class="location-container">
          <h3>{{chestermanS.title}}</h3>
          <b>{{chestermanS.swell}}</b>
        </div>
        <div class="location-container">
          <h3>{{wickaninnish.title}}</h3>
          <b>{{wickaninnish.swell}}</b>
        </div>
        <div class="location-container">
          <h3>{{coxBay.title}}</h3>
          <b>{{coxBay.swell}}</b>
        </div>
        <div class="location-container">
          <h3>{{Sombrio.title}}</h3>
          <b>{{Sombrio.swell}}</b>
        </div>
        <div class="location-container">
          <h3>{{jordanRiver.title}}</h3>
          <b>{{jordanRiver.swell}}</b>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'SurfSpots',
  data() {
    return{
      // Why does this work?
      longBeach: {},
      chestermanN: {},
      chestermanS: {},
      wickaninnish: {},
      coxBay: {},
      Sombrio: {},
      jordanRiver: {
        id:'',
        title:'',
        swell:'',
      },
    }
  },
  mounted () {
    this.fetchApi()
  },
  methods: {
    async fetchApi() {
      await axios.get('http://localhost:3000/spots') 
      .then((response)=>{
        //Long Beach
        this.longBeach.id = response.data[0].id,
        this.longBeach.swell = response.data[0].swell,
        this.longBeach.title = response.data[0].title
        //Chesterman Beach (North)
        this.chestermanN.id = response.data[1].id,
        this.chestermanN.swell = response.data[1].swell,
        this.chestermanN.title = response.data[1].title
        //Chesterman Beach (South)
        this.chestermanS.id = response.data[2].id,
        this.chestermanS.swell = response.data[2].swell,
        this.chestermanS.title = response.data[2].title
        //Wickaninnish
        this.wickaninnish.id = response.data[3].id,
        this.wickaninnish.swell = response.data[3].swell,
        this.wickaninnish.title = response.data[3].title
        //Cox Bay
        this.coxBay.id = response.data[4].id,
        this.coxBay.swell = response.data[4].swell,
        this.coxBay.title = response.data[4].title
        //Cox Bay
        this.Sombrio.id = response.data[5].id,
        this.Sombrio.swell = response.data[5].swell,
        this.Sombrio.title = response.data[5].title
        //Jordan River
        this.jordanRiver.id = response.data[6].id,
        this.jordanRiver.swell = response.data[6].swell,
        this.jordanRiver.title = response.data[6].title
      })
    }
  }
}
</script>

<style>
.main-container {
  background: #38A3A5;
  min-height: 100vh;
}

.main-container h1 {
    margin: 0;
    padding-top: 1.5rem;
}

.card-container {
  display: flex;
  justify-content: center;
  /* height: 100vh; */
}

.surf-spot-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  width: 100vw;
  /* height: 100%; */
  padding: 2rem 1rem;
  /* background: lightgreen; */
}

.location-container {
  /* display: flex;
  flex-direction: column;
  justify-content:center; */
  border: solid rgb(51, 66, 131) 2px;
  border-radius: 3px;
  background: #c7f9cc;
  height: 200px;
  width: 200px;
  margin: 10px;
}

.location-container h3 {
  padding-top: 16px;
}

.swell-size {
  display: flex;
}
</style>