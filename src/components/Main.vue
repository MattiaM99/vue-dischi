<template>
  <main>
    <div v-if="loading" class="container main-container">
      <albumsList
        v-for="(album, index) in albums"
        :key="index"
        :albums="album"/>
    </div>

     <Loading v-else titleLoader="Loading..."  />

  </main>
</template>

<script>
import axios from "axios";
import albumsList from "./Albums.vue";
import Loading from "./Loader.vue"

export default {
  name: "Main",
  components: {
    albumsList,
    Loading
  },
  data(){
    return{
      albums: [],
      api: "https://flynn.boolean.careers/exercises/api/array/music",
      loading : true
    }
  },
  methods:{
    getApi(){
      axios.get(this.api)
        .then( r => {
          this.albums = r.data.response;
          this.loading = true
        })
        .catch( e => {
          console.log(e);
        })
    }
  },
  mounted(){
    this.getApi();
  }
}
</script>

<style lang="scss">
@import "../assets/style/vars.scss";
main{
  height: calc(100vh - 150px);
  background-color: $secondary-color;
  .main-container{
    height: 100%;
    display: flex;
    flex-wrap: wrap;
    padding-top: 50px;
  }
}
</style>