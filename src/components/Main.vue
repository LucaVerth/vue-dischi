<template>
  <main>
    <div class="album-container py-5">
      <div class="container-fluid">
        <div class="row justify-content-center">
          <Cards
            v-for="(album, index) in filteredArray"
            :key="index"
            :album="album"
          />
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import axios from "axios";
import Cards from "./Cards.vue";

export default {
  components:{
    Cards,
  },
  props:{
    musicGenre: String,
  },
  data(){
    return{
      albums: [],
      apiData: 'https://flynn.boolean.careers/exercises/api/array/music'
    }
  },
  methods:{
    getData(){
      axios.get(this.apiData)
        .then(response =>{
          let data = response.data
          console.log(data);
          this.albums = data.response;
        })
        .catch(error =>{
          console.error(error);
        })
    }
  },
  computed:{
    filteredArray(){
      if(this.musicGenre === ''){
        return this.albums;
      }
      const filteredDiscs = [];
      this.albums.forEach( el => {
        if(el.genre === this.musicGenre)
        filteredDiscs.push(el)
      });
      return filteredDiscs;
    }
  },
  mounted(){
    this.getData();
  }
}
</script>

<style lang="scss">
@import '../assets/style/vars.scss';
@import '../assets/style/mixins.scss';

main{
  min-height: calc(100vh - 70px);
  background-color: $secondary-color;
  .album-container{
    display: flex;
    justify-content: center;
    width: 70%;
    margin: 0 auto;
  }
}
</style>