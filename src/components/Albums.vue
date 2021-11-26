<template>
  <div class="album-box">
    <img :src="albums.poster" :alt="albums.title">
    <h3>{{albums.title}}</h3>
    <h4>{{albums.author}}</h4>
    <h4>{{albums.year}}</h4>
  </div>
</template>

<script>
export default {
  name: "albumsList",
  props:{
    albums: Object
  }
}
</script>

<style lang="scss">
@import "../assets/style/vars.scss";
.album-box{
  width: calc(100% / 5 - 30px);
  cursor: pointer;
  margin: 15px;
  background-color: $primary-color;
  text-align: center;
  padding-bottom: 50px;
  padding: 15px;
  img{
    height: 50%;
    width: 100%;
    margin-bottom: 10px;
  }
  h3{
    color: white;
    margin-bottom: 10px;
    text-transform: uppercase;
  }
  h4{
    font-size: 15px;
    color: $artist-color;
  }
}
</style>