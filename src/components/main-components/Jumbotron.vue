<template>
    <!-- Sezione Jumbotron -->
    <div class="jumbotron w-100 d-flex flex-column justify-content-center align-items-center">
      <div class="container my-w60 d-flex flex-column justify-content-center align-items-center">
        <div class="jumbo-text d-flex flex-column align-items-center justify-content-center">
          <p class="mb-0">CONFERENCE ON</p>
          <p>SOCIAL NETWORKS</p>
        </div>
        <div class="info-bar w-50 mt-1">
          <div class="bar w-100"></div>
          <div class="bar-text fw-bold d-flex justify-content-between mt-2">
            <p>23-26 MAY 2019</p>
            <span>/</span>
            <p>SANS FRANCISCO</p>
            <span>/</span>
            <p>8 SPEAKERS</p>
          </div>
        </div>
        <button class="btn register-btn px-4 py-3 fw-bold mt-3">REGISTER ONLINE</button>
      </div>
    </div>
</template>

<script>
export default {
  name: 'Jumbotron',
  data () {
    return {
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../styles/generals.scss";

.jumbotron {
  height: 600px;
  background-image: url("../../assets/images/slider-1-bg.jpg");
  background-size: cover;
  background-position-y: center;

  .jumbo-text p {
    color: $white;
    font-size: 55px;
    font-weight: 300;
    letter-spacing: 2px;

    &:last-of-type {
      font-size: 85px;
      font-weight: 800;
      letter-spacing: 4px;
    }
  }
  .info-bar {
    .bar {
      height: 4px;
      background-color: $white;
    }
    .bar-text {
      padding: 0 1px;
      font-size: 18px;
      color: $white;
      
      span {
        font-weight: normal;
      }
    }
  }
  .register-btn {
    background-color: $scarlet;
    color: $white;
    letter-spacing: 2px;
    font-size: 16px;

    &:hover {
      background-color: $froly;
    }
  }
}

</style>
