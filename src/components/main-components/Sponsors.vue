<template>
    <!-- Sezione di Sponsor -->
    <div class="sponsors w-100 py-5">
      <div class="container my-w60 d-flex flex-column justify-content-center align-items-center">
        <h1 class="mt-3">SPONSORS</h1>
        <p class="text-center my-3">
          Maecenas faucibus mollis interdum. Nullam id dolor id nibh ultricies vehicula ut id elit.
        </p>
        <div class="row gx-5 sponsors-wrap w-100 my-4">
          <div v-for="(sponsor, index) in sponsors" :key="index"  class="my-card col-2">
          <img class="w-100" :src="require('../../assets/images/banner' + sponsor.path)" alt="">
          </div>
        </div>
      </div>
    </div>
</template>

<script>
import sponsorsImg from "../../data/sponsorsImg.js"

export default {
  name: 'Sponsors',
  data () {
    return {
      sponsors: sponsorsImg
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../styles/generals.scss";

.sponsors {
  background-color: #f6f6f6;
  h1 {
    font-weight: bold;
    letter-spacing: 2px;
  }
  p {
    color: $cloud;
    width: 40%;
  }
  img {
    cursor: pointer;
  }
}
</style>
