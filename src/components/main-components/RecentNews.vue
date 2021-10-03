<template>
    <!-- Sezione News Recenti -->
    <div class="recent-news my-w60 pb-5">
      <div class="recent-top w-100 d-flex align-items-center justify-content-between p-0 my-5">
        <h1 class="my-2">RECENT NEWS</h1>
        <a class="text-decoration-none red-link" href="#">Read All News</a>
      </div>
      <div class="container">
        <div class="row gx-4">
          <div v-for="(recent, index) in recentnews" :key="index"  class="news col-4 mb-3 d-flex flex-column">
            
            <div class="img-news-wrap">
              <img class="w-100" :src="require('../../assets/images/recent-news' + recent.path)" alt="">
              <div class="hover-sticky justify-content-center align-items-center">
                <i class="fas fa-bullhorn"></i>
                <div class="fw-bold">STICKY POST</div>
              </div>
            </div>
            <div class="news-info d-flex align-items-center mt-3 mb-0 p-0">
              <p>{{ recent.date }}</p>
              <p class="mx-3">/</p>
              <p>{{recent.comment}}<span> Comments </span></p>
            </div>
            <h3 class="fw-bold mt-0 mb-4">{{ recent.title.toUpperCase() }}</h3>
            <p class="news-text mb-4">
              {{ recent.text }}
            </p>
            <a class="text-decoration-none red-link" href="#">Read More</a>
          </div>
        </div>
      </div>

    </div>
</template>

<script>
import recentNews from "../../data/recentNews.js"

export default {
  name: 'RecentNews',
  data () {
    return {
      recentnews: recentNews
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../styles/generals.scss";

.recent-news {
  .recent-top {
    h1 {
      font-size: 30px;
      font-weight: bold;
      letter-spacing: 2px;
    }
  }
  .red-link {
    color: $scarlet;
    font-style: italic;
  }

  .news-info {
    color: $dustyGray;
    font-style: italic;
  }

  h3 {
    font-size: 20px;
  }

  .news-text {
    font-size: 14px;
    color: $gray;
  }

  .img-news-wrap {
    position: relative;
    .hover-sticky {
      display: none;
      position: absolute;
      right: 0;
      bottom: 0;
      width: 40%;
      height: 30px;
      font-weight: bold;
      font-size: 13px;
      background-color: black;
      color: white;
      i {
        margin-right: 5px;
      }
    }
    &:hover .hover-sticky {
      display: flex;
      cursor: pointer;
    }
  }
}
</style>
