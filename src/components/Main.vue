<template>
  <main>
    <!-- Sezione Jumbotron -->
    <Jumbotron />
    <CompanyInfo />
    <Subscribe />
    <Speakers />
    <Program />
  </main>
</template>

<script>
import Jumbotron from './main-components/Jumbotron.vue'
import CompanyInfo from './main-components/CompanyInfo.vue'
import Subscribe from './main-components/Subscribe.vue'
import Speakers from './main-components/Speakers.vue'
import Program from './main-components/Program.vue'

export default {
  name: 'Main',
  components: {
    Jumbotron,
    CompanyInfo,
    Subscribe,
    Speakers,
    Program
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
