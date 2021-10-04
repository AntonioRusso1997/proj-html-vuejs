<template>
    <!-- Sezione di Presentation -->
    <div class="presentation w-100 py-5">
      <div class="container py-3 my-w60 my-4">
        <div class="row w-100">
          <div class="pres-section col-6 p-3 d-flex flex-column">
            <h1>PRESENTATION</h1>
            <div class="video-wrap w-100 d-flex justify-content-center">
              <img class="video-img" src="../../assets/images/461365506.jpeg" alt="Presentation img">
              <div class="video-player w-100 d-flex align-items-center">
                <div class="play-icon d-flex justify-content-center align-items-center"><i class="fas fa-play"></i></div>
                <div class="play-bar">
                  <div class="video-time d-flex justify-content-center align-items-center p-0 m-0">
                    <div class="p-0 m-0">
                      <p class="p-0 m-0">1:01:26</p>
                      <div class="little-square"></div>
                    </div>
                  </div>
                </div>
                <div class="volume d-flex justify-content-center align-items-end">
                  <div></div>
                  <div></div>
                  <div></div>
                  <div></div>
                  <div></div>
                </div>
                <div class="set-icon d-flex justify-content-center align-items-center"><i class="fas fa-cog"></i></div>
                <img src="../../assets/images/vimeo.png" alt="Vimeo logo">                
              </div>
            </div>
          </div>
          <div class="twitter-section col-6 p-3 d-flex flex-column">
            <h1>TWITTER FEED</h1>
            <div v-for="(tweet, index) in tweets" :key="index" class="tweet w-100 my-3 d-flex">
              <i class="fab fa-twitter"></i>
              <div class="tweet-wrap my-0 d-flex flex-column">
                <p class="tweet-text my-0">
                  {{ tweet.text }} <a class="text-decoration-none" href="#">{{tweet.link}}</a>
                </p>
                <div class="tweet-date mt-2">{{ tweet.date }}</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
import tweet from "../../data/tweet.js"

export default {
  name: 'Presentation',
  data () {
    return {
      tweets: tweet
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../styles/generals.scss";

.presentation {
  
  h1 {
    font-size: 30px;
    font-weight: bold;
    letter-spacing: 2px;
    margin-bottom: 30px;
  }

  .pres-section {
    .video-wrap {
      position: relative;

      .video-img {
        width: 90%;
      }
      .video-player {
        position: absolute;
        bottom: 10px;
        left: 0;
        background-color: black;
        border-radius: 5px;
        color: white;
        height: 40px;
        padding: 5px;
        .play-icon {
          height: 100%;
          width: 10%;
          font-size: 20px;
          i {
          cursor: pointer;
          }
        }
        .play-bar {
          position: relative;
          cursor: pointer;
          height: 40%;
          padding: 0 10px;
          width: 75%;
          border: 1px solid $cloud;

          .video-time {
            position: absolute;
            width: 40px;
            top: -22px;
            left: -20px;
            background-color: white;
            font-size: 12px;
            color: black;

            div {
              position: relative;
              p {
                z-index: 999;
              }
              .little-square {
                position: absolute;
                bottom: -2px;
                left: 13px;
                width: 10px;
                height: 10px;
                transform: rotate(45deg);
                // background-color: white;
              background: linear-gradient(90deg, transparent 50%, white 50%);
              }
            }

          }
        }
        .volume {
          height: 50%;
          width: 10%;
          padding: 0 8px;
          div {
            cursor: pointer;
            width: calc((100% / 5) - 2px);
            background-color: $gray;
            margin: 0 1px;
            &:nth-last-of-type(1) {
              height: 100%;
            }
            &:nth-last-of-type(2) {
              height: 80%;
              background: linear-gradient(90deg, #43bceb 50%, $gray 50%);
            }
            &:nth-last-of-type(3) {
              height: 60%;
              background-color: #43bceb;
            }
            &:nth-last-of-type(4) {
              height: 40%;
              background-color: #43bceb;
            }
            &:nth-last-of-type(5) {
              height: 20%;
              background-color: #43bceb;
            }
          }
                  
        }
        .set-icon {
          width: 5%;
          height: 100%;
          i {
          cursor: pointer;
          }
        }
        img {
          cursor: pointer;
          height: 20px;
          margin-bottom: 3px;
          padding: 0 2px;
        }
      }
    }
  }

  .twitter-section {
    .tweet {

      i {
        font-size: 25px;
        color: #43bceb;
      }

      .tweet-wrap {
          margin-left: 20px;
          font-size: 14px;
          color: $gray;
          a {
            color: $scarlet;
          }
          
          div {
            color: $cloud;
            font-style: italic;
          }
      }
    }
  }
}
</style>