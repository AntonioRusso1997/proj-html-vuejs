<template>
    <!-- Sezione di Iscrizione Newsletter -->
    <div class="subscribe w-100 d-flex justify-content-center align-items-center">
      <div class="container w-50 d-flex flex-column align-items-center justify-content-between">
        <div class="countdown w-60 px-5 mb-5 d-flex justify-content-center align-items-center w-100">
          <div class="rectangle d-flex flex-column justify-content-center align-items-center">
            <div class="count-number">3399</div>
            <div class="count-text">DAYS</div>
          </div>
          <div class="square d-flex flex-column justify-content-center align-items-center">
            <div class="count-number">17</div>
            <div class="count-text">HOURS</div>
          </div>
          <div class="square d-flex flex-column justify-content-center align-items-center">
            <div class="count-number">28</div>
            <div class="count-text">MINS</div>
          </div>
          <div class="square d-flex flex-column justify-content-center align-items-center">
            <div class="count-number">17</div>
            <div class="count-text">SECS</div>
          </div>
        </div>
        <h2>SUBSCRIBE FOR UPDATES</h2>
        <div class="sub-form w-60 mt-4 d-flex justify-content-center align-items-center">
          <input class="sub-input border-0 w-50" placeholder="Please fill your email" type="email">
          <button class="btn-square .sub-btn">SUBSCRIBE</button>
        </div>
      </div>

    </div>
</template>

<script>
export default {
  name: 'Subscribe',
  data () {
    return {
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../styles/generals.scss";

.subscribe {
  height: 500px;
  background-image: url("../../assets/images/coutdown-bg1.jpg");
  background-size: cover;
  background-position-y: -80px;

  .countdown {
    .rectangle, .square {
      height: 150px;
      border-radius: 10px;
      background-color: $black;
      margin: 0 10px;
      padding-bottom: 10px;
      color: $white;

      .count-number {
        font-size: 50px;
        font-weight: bold;
      }
    }
    .rectangle {
      width: 25%;
      opacity: 80%;
    }
    .square {
      width: 20%;
      &:nth-last-child(3) {
        opacity: 70%;
      }
      &:nth-last-child(2) {
        opacity: 60%;
      }
      &:nth-last-child(1) {
        opacity: 50%;
      }
    }
  }
  h2 {
    font-size: 22px;
    font-weight: 900;
    letter-spacing: 4px;
  }
  .sub-form {
    width: 80%;

    .sub-input {
      margin-right: 10px;
      font-size: 18px;
      padding: 10px;

      &::placeholder {
        font-size: 14px;
      }
    }
    .sub-btn {
      font-size: 18px;
      padding: 10px 0;
    }
  }
}

</style>
