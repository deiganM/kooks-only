<template>
  <div class="main-container">
    <div class="surf-spot-container">
      <div class="location-container">
        <h3>{{longBeach.title}}</h3>
        <p>Swell Size</p>
        <b>{{longBeach.swell}}</b>
      </div>
      <div class="location-container">
        <h3>{{chestermanN.title}}</h3>
        <p>Swell Size</p>
        <b>{{chestermanN.swell}}</b>
      </div>
      <div class="location-container">
        <h3>{{chestermanS.title}}</h3>
        <p>Swell Size</p>
        <b>{{chestermanS.swell}}</b>
      </div>
      <div class="location-container">
        <h3>{{wickaninnish.title}}</h3>
        <p>Swell Size</p>
        <b>{{wickaninnish.swell}}</b>
      </div>
      <div class="location-container">
        <h3>{{coxBay.title}}</h3>
        <p>Swell Size</p>
        <b>{{coxBay.swell}}</b>
      </div>
      <div class="location-container">
        <h3>{{Sombrio.title}}</h3>
        <p>Swell Size</p>
        <b>{{Sombrio.swell}}</b>
      </div>
      <div class="location-container">
        <h3>{{jordanRiver.title}}</h3>
        <p>Swell Size</p>
        <b>{{jordanRiver.swell}}</b>
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
      spots: [],
      longBeach: {
        id:'',
        title:'',
        swell:'',
      },
      chestermanN: {
        id:'',
        title:'',
        swell:'',
      },
      chestermanS: {
        id:'',
        title:'',
        swell:'',
      },
      wickaninnish: {
        id:'',
        title:'',
        swell:'',
      },
      coxBay: {
        id:'',
        title:'',
        swell:'',
      },
      Sombrio: {
        id:'',
        title:'',
        swell:'',
      },
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
  /* display: flex;
  justify-content: center; */
  border: solid rgb(51, 66, 131) 2px;
  height: 200px;
  width: 200px;
  margin: 10px;
}
</style>