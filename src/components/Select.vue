<template>
  <div class="genere">
    <select
      v-model="selected"
      @select="$emit('music', selected)"
      name="" id="">
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
  methods:{
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
  }
}
</style>