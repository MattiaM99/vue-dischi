<template>
  <header>
    <h1>LOGO</h1>
    <Select @select="search"/>
  </header>
</template>

<script>
import Select from "./Select.vue";
export default {
  name: "Header",
  data(){
    return{
      genereDisco: ""
    }
  },
  components: {
    Select
  },
  methods: {
    checkSearch(music){
      this.genereDisco = music;
      console.log(music);
    }
  }
}
</script>

<style lang="scss">
@import "../assets/style/vars.scss";
header{
  background-color: $primary-color;
  height: 150px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  h1{
    margin-left: 20px;
    color: green;
  }
}
</style>