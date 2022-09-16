<template>
  <div>
    <navbar />
    <div class="main-page" >
      <div class="gasoline">
        
        <div>
          <gasoline />
        </div>
        <div class="addBtnClass">
          <button class="addBtn btn btn-outline-success mr-2 my-2 my-sm-0">ADD TRACKER</button>
          <button class="addBtn2 btn btn-outline-success mr-2 my-2 my-sm-0">THIS HIDDEN</button>
        </div>
      </div>

        <denem2 />
      <div v-if="tracker != null" class="ifContainer">
        <mainCard v-for="product in tracker" 
        :key="product.result"  
        :product="product"
        :hal="hal"
        :isim="isim"
        :ortalama="(max+min)/2" />
      </div>

      <!-- <div v-if="tracker != null" class="ifContainer">
        <trackerCard v-for="product in tracker" 
        :key="product.result"  
        :product="product"
        :hal="hal"
        :isim="isim" />
      </div> -->

      <!-- <div v-if="tracker != null" class="bazaar">
        <h1>{{tracker.isim}}</h1>
      </div> -->
  
    </div>
  </div>
  
</template>

<script>
import Navbar from "../components/navbar.vue";
import TrackerCard from "../components/trackerCard.vue";
import Gasoline from "../components/gasoline.vue";
import MainCard from "../components/mainCard.vue";

const baseURL = "https://api.collectapi.com/bazaar/single?city=istanbul";
const axios   = require('axios').default; //AXİOS ERROR

export default {
  name: 'IndexPage',
  data:() => ({
    tracker: null
  }),

  created() {
    this.getBazaar()
  },

  methods: {
    refreshPage() {
      window.location.reload();
    },
    async getBazaar() {
      await axios.get(`${baseURL}`, {
        headers: {
          "content-type": "application/json",
          "authorization": "apikey 5stBOgPqyRYAHlJ2ero7uf:4RasQjjOgwLTpDfEovVmNk"
          // apikey 5stBOgPqyRYAHlJ2ero7uf:4RasQjjOgwLTpDfEovVmNk
        }
      })   
      .then(response => {
        this.tracker = response.data.result
        console.log(this.tracker)
      })
      .catch(error => {
        console.log(error)
      })
    }
  },
  components: { TrackerCard, Gasoline, MainCard, Navbar }
}
</script>





<style scoped>
.main-page {
  background: #E5E5E5;
  display: flex;
  flex-direction: column;
}
.ifContainer {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  margin-top: 20px;
}
.gasoline {
  height: 22vh auto;
  background: #E5E5E5;
  /* border: 1px solid black; */
  display: flex;
  flex-direction: column;
}
.addBtn {
  margin: 10px;
}
.addBtn2 {
  visibility: hidden;
}
.addBtnClass {
  display: flex;
  justify-content: end;
  margin-bottom: 10px;

}
</style>
