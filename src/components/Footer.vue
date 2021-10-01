<template>
  <footer class="d-flex flex-column">
    <div class="footer-top container my-w60">
      <div class="row my-3">
      <div class="col-3 py-4">
        <h4 class="mb-4">ABOUT US</h4>
        <p>Cum sociis natque penatibus et magnis dis parturient montes, nascetur ridiculus mus</p>
        <div class="social d-flex justify-content-between text-white my-4">
          <i class="fab fa-facebook-square"></i>
          <i class="fab fa-twitter-square"></i>
          <i class="fab fa-linkedin"></i>
          <i class="fab fa-google-plus-square"></i>
          <i class="fab fa-pinterest-square"></i>
          <i class="fab fa-flickr"></i>

        </div>
      </div>
      <div class="col-3 py-4">
        <h4 class="mb-4">RECENT NEWS</h4>
        <ul class="list-unstyled" v-for="(item, index) in items" :key="index">
          <li class=""><a class="text-decoration-none" :href="item.url">{{ item.text.toUpperCase() }}</a></li>
        </ul>
      </div>
      <div class="col-3 py-4">
        <h4 class="mb-4">GET YOUR SEAT!</h4>
        <p>
          Book for your seat before it's too rate.
          We provide variety of ticket option.
        </p>
        <button class="footer-btn my-2">CHECK OUT TICKETS!</button>

      </div>
      <div class="col-3 py-4">
        <h4 class="mb-4">GALLERY FROM LAST YEAR</h4>
        <div class="container p-0">
          <div class="row w-100 p-0">
            <img v-for="(image, index) in images" :key="index" class="col-3 p-1" :src="require('../assets/' + image.path)" alt="">
          </div>
        </div>

      </div>
      </div>
    </div>
    <div class="footer-bottom">
      <div class="d-flex justify-content-between align-items-center pt-3 h-100 my-w60">
        <p>© Copyright GoodLayers, All Right Reserved</p>
        <ul class="d-flex list-unstyled">
          <li><a href="#">About Us</a></li>
          <div>|</div>
          <li><a href="#">Accommodation</a></li>
          <div>|</div>
          <li><a href="#">Call For Paper</a></li>
          <div>|</div>
          <li><a href="#">Contact Us</a></li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
import footerNav from "../data/footerNav.js"
import footerImg from "../data/footerImg.js"
export default {
  name: 'Footer',
  data() {
    return {
      items: footerNav,
      images: footerImg,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../styles/generals.scss";
footer {
  height: 400px;
  background-color: $mineShaft;

  .footer-top {
    height: calc(100% - 70px);

    h4 {
      color: $cloud;
      font-weight: 600;
      font-size: 15px;
    }
    p {
      color: $cloud;
      font-size: 15px;
    }

    .social {
      width: 80%;
      font-size: 25px;
    }

    ul li a {
      font-size: 13px;
      color: $gray;
      &::before {
        font-size: 12px;
        content: 	">";
        margin-right: 10px;
      }
    }
    
    .footer-btn {
      font-size: 13px;
      font-weight: bold;
      padding: 10px 20px;
      background-color: $scarlet;
      border: none;
      border-bottom: 3px solid $froly;
      color: $white;

      &:hover {
        background-color: $froly;
      }
    }
  }
  .footer-bottom {
    height: 70px;
    background-color: $black;
    font-size: 14px;

    p {
      color: $gray;
    }
    ul{
      color: $cloud;
      
      li a {
        text-decoration: none;
        color: $cloud;
        margin: 0 3px;
      }
    } 
  }
}
</style>
