<template>
  <div>
    <Header />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Footer
  }
}
</script>

<style lang="scss">
@import "./styles/generals.scss";
@import '~@fortawesome/fontawesome-free/css/all.min.css';

</style>
