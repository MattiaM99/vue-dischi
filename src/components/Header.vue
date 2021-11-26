<template>
  <header>
    <h1>LOGO</h1>
  </header>
</template>

<script>
export default {
  name: "Header"
}
</script>

<style lang="scss">
@import "../assets/style/vars.scss";
header{
  background-color: $primary-color;
  height: 150px;
  display: flex;
  align-items: center;
  h1{
    margin-left: 20px;
    color: green;
  }
}
</style>