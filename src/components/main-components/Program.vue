<template>
    <!-- Sezione Program -->
    <div class="program w-100">
      <div class="container my-w60 py-5">
        <div class="program-top px-0 my-5 w-100 d-flex align-items-center">
          <h1>PROGRAM</h1>
          <p class="w-50 mx-5">This conference run through all 4 days from 23-26 May 2016. <br>
            We also provide free lunch and coffee break in each day.
          </p>
          <p class="mx-0"><a class="text-decoration-none" href="#">View Full Program</a></p>
        </div>
        <div class="calendar w-100 mx-2 mb-4">
          <div class="row row-days mb-0">
            <div v-for="(day, index) in days" :key="index" class="col-2 d-flex flex-column justify-content-center">
              <h3 class="m-0">{{ day.nmb.toUpperCase() }}</h3>
              <p class="m-0"><span>{{ day.date }}</span> May 2016</p>
            </div>
            <div class="col-2"></div>
          </div>
          <div class="row row-main mt-0 py-1">
            <div class="col-left col-3 p-5 d-flex flex-column">
              <div><i class="far fa-clock"></i> <span>09:00 - 10:30</span></div>
              <div><i class="fas fa-location-arrow"></i><span>ROOM A</span></div>
              <div><i class="fas fa-user"></i><span>LAURENCE FRANCIS</span></div>
            </div>
            <div class="col-right col-9 p-5 d-flex flex-column">
              <h2 class="mb-3">WELCOMING AND INTRODUCTION</h2>
              <p class="mb-3">
                Vestibulum id ligula porta felis euismod semper. Nullam quis risus eget urna mollis ornare vel eu leo. Donec ullamcorper nulla non metus auctor fringilla. Aenean lancinia bibendum nulla sed consectetur....
              </p>
              <img class="mt-3 mb-2" src="../../assets/images/speaker-8-150x150.jpg" alt="speaker img">
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'Program',
  data () {
    return {
      days: [
        {
          nmb: 'Day 1',
          date: 23
        },
        {
          nmb: 'Day 2',
          date: 23
        },
        {
          nmb: 'Day 3',
          date: 24
        },
        {
          nmb: 'Day 4',
          date: 25
        },
        {
          nmb: 'Day 5',
          date: 26
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../styles/generals.scss";

.program-top {
  position: relative;
  h1 {
    font-weight: bold;
    letter-spacing: 2px;
  }
  p {
    font-size: 16px;

    &:last-of-type {
      position: absolute;
      right: 0;
      font-style: italic;
      
      a {
        color: $scarlet;
      }
    }
  }
}
.row-days {
  div {
    font-family: sans-serif;
    background-color: $scarlet;
    border-left: 1px solid $thunderbird;
    color: white;
    padding: 15px 25px;

    &:first-child {
      border: none;
      background-color: $thunderbird;
    }
    h3 {
      font-size: 18px;
      font-weight: bold;
      letter-spacing: 0;
    }
    p {
      font-size: 14px;
    }
  }
}
.row-main {
  background-color:#f7f7f7;

  .col-left {
    div {
      margin-bottom: 15px;
      font-size: 12px;
      color: $gray;
      display: flex;
      align-items: center;

      span:first-of-type {
        font-size: 14px;
      }
  
      i {
        font-size: 14px;
        margin-right: 20px;     
      }
    }
  }

  .col-right {
    h2 {
      font-size: 20px;
      letter-spacing: 4px;
      font-weight: 700;
    }
    p {
      font-size: 14px;
      color: $gray;
    }
    img {
      height: 50px;
      width: 50px;
    }
  }
}
</style>
