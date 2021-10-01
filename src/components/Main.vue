<template>
  <main>
    <!-- Sezione Jumbotron -->
    <div class="jumbotron w-100">
      <div class="">CONFERENCE ON</div>
      <div class="">SOCIAL NETWORKS</div>
      <div class="info-bar">
        <div class="bar"></div>
        <p>23-26 MAY 2019</p>
        <span>/</span>
        <p>SANS FRANCISCO</p>
        <span>/</span>
        <p>8 SPEAKERS</p>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: 'Main',
  data () {
    return {
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../styles/generals.scss";

.jumbotron {
  height: 600px;
  background-image: url("../assets/images/slider-1-bg.jpg");
  background-size: cover;
  background-position-y: center;
}

</style>
