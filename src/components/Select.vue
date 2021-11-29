<template>
  <div class="genere">
    <select
      v-model="select"
      @select="$emit('music', select)"
      name="" id="" >
      <option selected disabled hidden value="">Seleziona genere</option>
      <option value="rock">Rock</option>
      <option value="pop">Pop</option>
      <option value="jazz">Jazz</option>
      <option value="metal">Metal</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "Select",
  data(){
    return{
      music: ""
    }
  },
  computed:{
    select(){
      return this.music
    }
  }
}
</script>

<style lang="scss">
.genere{
  select{
    padding: 15px 20px;
    font-weight: bold;
    margin-right: 15px;
  };
  option{
    color: black;
  }
}
</style>