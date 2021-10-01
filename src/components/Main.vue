<template>
  <main>
    <!-- Sezione Jumbotron -->
    <Jumbotron />
    <CompanyInfo />
    <Subscribe />
  </main>
</template>

<script>
import Jumbotron from './main-components/Jumbotron.vue'
import CompanyInfo from './main-components/CompanyInfo.vue'
import Subscribe from './main-components/Subscribe.vue'

export default {
  name: 'Main',
  components: {
    Jumbotron,
    CompanyInfo,
    Subscribe
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
