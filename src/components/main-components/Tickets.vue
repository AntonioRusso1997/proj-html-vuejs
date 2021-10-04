<template>
    <!-- Sezione dei Tickets -->
    <div class="tickets w-100 d-flex flex-column justify-content-center align-items-center">
      <h1>TICKETS</h1>
      <div class="container my-w60 d-flex flex-column justify-content-center align-items-center p-0">
        <div class="row w-100">
          <div v-for="(ticket, index) in tickets" :key="index" class="ticket col-4 d-flex flex-column justify-content-center align-items-center px-3">
            <div class="ticket-top w-100 d-flex flex-column justify-content-center align-items-center p-4 m-0">
              <h2 class="fw-bold mt-2">{{ ticket.name.toUpperCase() }}</h2>
              <h3 class="fw-bold">{{ ticket.price }}</h3>
              <div :class="ticket.featured == true ? 'd-flex' : 'd-none'" class="featured-sticker align-item-center justify-content-center p-1">Featured!</div>                           
            </div>
            <div class="ticket-info w-100 d-flex justify-content-center align-items-center p-4 m-0">
              <ul class="d-flex p-0 flex-column justify-content-center align-items-center">
                <li>{{ ticket.dayN }} Access</li>
                <li>Coffee Break</li>
                <li>Lunch(International Buffet)</li>
                <li>Document Sheets</li>
                <li>{{ ticket.voucher }} Voucher For Next Event</li>
              </ul>
            </div>
            <div class="ticket-bottom w-100 d-flex justify-content-center align-items-center p-3 m-0">
              <h3>BOOK NOW</h3>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
import ticketInfo from "../../data/ticketInfo.js"

export default {
  name: 'Ticket',
  data () {
    return {
      tickets: ticketInfo
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../styles/generals.scss";

.tickets {
  height: 650px;
  background-image: url(../../assets/images/ticket-bg.jpg);
  background-size: cover;    

  h1{
    font-weight: bold;
    letter-spacing: 2px;
    margin-bottom: 50px;
    color: $white;
  }

  h2,h3 {
    margin: 0;
  }
  
  .ticket-top {
    position: relative;
    background-color:#e9e9e9;
    overflow: hidden;
    h2 {
      font-size: 20px;
    }
    h3 {
      font-size: 18px;
      color: $scarlet;
    }
    .featured-sticker {
      position: absolute;
      top: 20px;
      right: -40px;
      width: 150px;
      background-color: $scarlet;
      color: white;
      font-size: 14px;
      transform: rotate(45deg);
    }
  }
  
  .ticket-info {
    background-color: $white;
    color: $gray;
    ul {
      list-style: none;
      margin: 10px 0;
      
      li {
        margin: 5px 0;
        font-size: 14px;
        font-style: italic;
        font-weight: 600;
      }
    }
  }
  
  .ticket-bottom {
    background-color: $scarlet;
    color: white;

    h3 {
      font-size: 14px;
      font-weight: bold;
    }
  }
}
</style>