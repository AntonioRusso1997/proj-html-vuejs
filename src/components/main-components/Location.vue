<template>
    <!-- Sezione Location -->
    <div class="location w-100 d-flex flex-column justify-content-center align-items-center text-white">
      <div class="container w-50 d-flex flex-column justify-content-center align-items-center">
        <h1 class="fw-bold">LOCATION</h1>
        <h3 class="fw-bold mb-2">GD BUILDING, GRAND CONFERENCE ROOM</h3>
        <p class="mb-3"><i class="fas fa-location-arrow"></i> 11 GD Building, River Mall, New York, USA 8879</p>
        <label class="mb-2" for="location">Check For Accommodations Here</label>
        <input class="w-50 mb-1" type="text" id="location">
        <div class="w-50 d-flex justify-content-between align-items-center">
          <p><i class="fas fa-phone-alt"></i> +1-112-222-3344</p>
          <p><i class="fas fa-envelope"></i> Contact@TheKeynoteTheme.com</p>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'Location',
  data () {
    return {
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../styles/generals.scss";

.location {
  height: 420px;
  background-image: url(../../assets/images/location-bg.jpg);
  background-size: cover;

  h1 {
    letter-spacing: 2px;
    margin-bottom: 50px;

  }

  h3 {
    font-size: 22px;
    letter-spacing: 6px;
  }

  label {
    color: $scarlet;
  }

  input {
    background: transparent;
    border: none;
    border-bottom: 3px solid white;
    font-size: 22px;
    color: white;

    &:focus {
      border: none;
    }
  }

  i {
    margin-right: 10px;
    font-size: 14px;
  }
}

</style>
