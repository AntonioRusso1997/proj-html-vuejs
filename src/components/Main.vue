<template>
  <main>
    <!-- Sezione Jumbotron -->
    <Jumbotron />
    <CompanyInfo />
    <Subscribe />
    <Speakers />
    <Program />
    <Map />
    <Location />
    <RecentNews />
    <Tickets />
    <Sponsors />
  </main>
</template>

<script>
import Jumbotron from './main-components/Jumbotron.vue'
import CompanyInfo from './main-components/CompanyInfo.vue'
import Subscribe from './main-components/Subscribe.vue'
import Speakers from './main-components/Speakers.vue'
import Program from './main-components/Program.vue'
import Map from './main-components/Map.vue'
import Location from './main-components/Location.vue'
import RecentNews from './main-components/RecentNews.vue'
import Tickets from './main-components/Tickets.vue'
import Sponsors from './main-components/Sponsors.vue'

export default {
  name: 'Main',
  components: {
    Jumbotron,
    CompanyInfo,
    Subscribe,
    Speakers,
    Program,
    Map,
    Location,
    RecentNews,
    Tickets,
    Sponsors
  },
  data () {
    return {
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../styles/generals.scss";

</style>
