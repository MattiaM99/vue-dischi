<template>
<div class="loader">
  <h3>{{titleLoader}}</h3>
  <div class="lds-ellipsis"><div></div><div></div><div></div><div></div></div>
</div>
</template>

<script>
export default {
  name: "Loading",
  props:{
    titleLoader: String
  }
}
</script>

<style lang="scss" scoped>

@import '../assets/style/vars.scss';

.loader{
  padding-top: 10%;

  .lds-ellipsis div:nth-child(2) {
  left: 8px;
  animation: lds-ellipsis2 0.6s infinite;
  }
  .lds-ellipsis div:nth-child(3) {
    left: 32px;
    animation: lds-ellipsis2 0.6s infinite;
  }
  .lds-ellipsis div:nth-child(4) {
    left: 56px;
    animation: lds-ellipsis3 0.6s infinite;
  }
  @keyframes lds-ellipsis1 {
    0% {
      transform: scale(0);
    }
    100% {
      transform: scale(1);
    }
  }
  @keyframes lds-ellipsis3 {
    0% {
      transform: scale(1);
    }
    100% {
      transform: scale(0);
    }
  }
  @keyframes lds-ellipsis2 {
    0% {
      transform: translate(0, 0);
    }
    100% {
      transform: translate(24px, 0);
    }
  }
}
</style>