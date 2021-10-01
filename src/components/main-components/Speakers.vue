<template>
    <!-- Sezione Speakers -->
    <div class="speakers w-100 d-flex justify-content-center">
      <div class="container my-w60 d-flex flex-column justify-content-center">
        <div class="w-100 d-flex justify-content-between position-relative">
          <h1>SPEAKERS</h1>
          <div class="arrows d-flex align-items-center">
            <button class="btn btn-arrow"><i class="fas fa-chevron-left"></i></button>
            <button class="btn btn-arrow"><i class="fas fa-chevron-right"></i></button>
          </div>
        </div>
        <div class="row w-100 py-4">
          <div v-for="(speaker, index) in speakers" :key="index" class="speaker-card p-3 col-3 d-flex flex-column align-items-center justify-content-center">
            <img class="w-100 my-2" :src="require('../../assets/' + speaker.path)" alt="">
            <div class="speaker-name mt-3">{{speaker.name.toUpperCase()}}</div>
            <div class="speaker-job">{{speaker.job}}</div>

          </div>
        </div>



      </div>
    </div>
</template>

<script>
import speakersList from "../../data/speakersList.js"

export default {
  name: 'Speakers',
  data () {
    return {
      speakers: speakersList
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../styles/generals.scss";

.speakers {
  height: 500px;
  background-color: #f3f3f3;

  h1 {
    font-style: 30px;
    font-weight: bold;
    letter-spacing: 2px;
  }

  .arrows {

    .btn-arrow {
      padding: 10px 12px;
      font-size: 10px;
      font-weight: 300;
      background-color: $scarlet;
      margin: 2px;
      color: white;
    }
  }
  .speaker-name {
    font-size:15px;
    font-weight: 600;
    letter-spacing: 2px;
  }
  .speaker-job {
    font-size: 14px;
    font-weight: 500;
    font-style: italic;
    color: $gray;
  }
}

</style>
