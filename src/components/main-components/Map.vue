<template>
    <!-- Sezione Della Mappa -->
    <div class="map w-100 p-0 mb-2 position-relative">
      <div class="container-fluid w-100 p-0">
        <div class="map-row d-flex flex-wrap w-100 p-0">
          <div v-for="(map, index) in maps" :key="index" class="my-col m-0 p-0">
            <img class="w-100" :src="require('../../assets/images/map' + map.path)" alt="Map">
          </div>
        </div>
      </div>
      <div class="map-select btn btn-group d-flex align-items-center">
        <label class="btn btn-light fw-bold">Map</label>
        <label class="btn btn-light">Satellite</label>
      </div>
      <img class="google-logo" src="../../assets/images/google4.png" alt="Google Logo">
      <div class="google-icons d-flex flex-column justify-content-center align-items-center">
        <div class="btn btn-light omino"><img src="../../assets/images/image (4).svg" alt="man icon"></div>
        <div class="btn btn-group mt-4 d-flex flex-column justify-content-center align-items-center">
          <label class="btn btn-light"><img src="../../assets/images/image (7).svg" alt="-"></label>
          <label class="btn btn-light"><img src="../../assets/images/image (8).svg" alt="+"></label>
        </div>
      </div>

    </div>
</template>

<script>
import mapImg from "../../data/mapImg.js"

export default {
  name: 'Map',
  data () {
    return {
      maps: mapImg
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../styles/generals.scss";

.map {
  .my-col {
    width: calc(100% / 8);
  }

  .map-select {
    position: absolute;
    top: 0;
    left: 0;
    margin: 10px 5px;

    label {
      font-size: 18px;
        &:first-of-type {
          position: relative;
          &:before {
            content : "";
            position: absolute;
            right: 0;
            bottom: 0;
            height: 100%;
            width: 1px;
            border-right:1px solid black;
            opacity: 40%;
          }
        }
    }
  }
  
  .google-logo {
    position: absolute;
    left: 0;
    bottom: 0;
    margin: 5px;
  }
  
  .google-icons {
    position: absolute;
    right: 0;
    bottom: 0;
    margin: 20px 10px;

    .omino {
      img {
        width: 18px;
      }
    }

    .btn-group .btn-light:first-child {
      position: relative;
      &:before {
      content : "";
      position: absolute;
      left: 50%;
      transform: translateX(-50%);
      bottom: 0;
      height: 1px;
      width: 70%;
      border-bottom:1px solid black;
      opacity: 40%;
      }
    }
  }
}
</style>
