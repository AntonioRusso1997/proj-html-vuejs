<template>
    <!-- Sezione Informazioni -->
    <div class="company w-100 py-5">
      <div class="container my-w60 py-3">
        <div class="row w-100">
          <div class="info-card col-4 d-flex">
            <i class="fas fa-trophy"></i>
            <div class="info-card-wrap d-flex flex-column">
              <h4>WHO WE ARE</h4>
              <p>Donec id elit non mi porta gravida at eget me tus. Sed posuere consectetur estat lobo rtis. Cum sociis natoque.</p>
              <a href="#">Learn More</a>
            </div>
          </div>
          <div class="info-card col-4 d-flex">
            <i class="fas fa-bolt"></i>
            <div class="info-card-wrap d-flex flex-column">
              <h4>WHO WE ARE</h4>
              <p>Donec id elit non mi porta gravida at eget me tus. Sed posuere consectetur estat lobo rtis. Cum sociis natoque.</p>
              <a href="#">Learn More</a>
            </div>
          </div>
          <div class="info-card col-4 d-flex">
            <i class="fas fa-question"></i>
            <div class="info-card-wrap d-flex flex-column">
              <h4>WHO WE ARE</h4>
              <p>Donec id elit non mi porta gravida at eget me tus. Sed posuere consectetur estat lobo rtis. Cum sociis natoque.</p>
              <a href="#">Learn More</a>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'CompanyInfo',
  data () {
    return {
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../styles/generals.scss";

.info-card {

  i {
    font-size: 24px;
    color: $cloud;
    margin-right: 40px;
  }
  .info-card-wrap {
    h4 {
      font-size: 15px;
      font-weight: 700;
      letter-spacing: 2px;
      margin-top:5px;
      margin-bottom: 30px;
    }
    p {
      font-size: 14px;
      color: $dustyGray;
    }
    a {
      text-decoration: none;
      font-style: italic;
      font-size: 15px;
      color: $scarlet;
      margin-top: 10px;
    }
    
  }
}
</style>
