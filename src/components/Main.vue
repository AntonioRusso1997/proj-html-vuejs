<template>
  <main>
    <!-- Sezione Jumbotron -->
    <Jumbotron />
  </main>
</template>

<script>
import Jumbotron from './Jumbotron.vue'

export default {
  name: 'Main',
  components: {
    Jumbotron
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
