<template>
  <header class="d-flex align-items-center justify-content-between my-w60 p-3">
    <a class="text-decoration-none" href="/">
    <img src="../assets/images/logo.png" alt="The Keynote Logo">
    </a>

    <!-- Navbar che compilerò tramite js -->
    <nav>
      <ul class="d-flex list-unstyled align-items-center mt-4">
        <li v-for="(item, index) in items" :key="index"><a :class="(item.current) ? 'active' : null" class="text-decoration-none py-2 px-1 mx-3" :href="item.url">{{ item.text.toUpperCase() }}</a></li>
        <span class="mx-3">|</span>
        <a class="text-decoration-none" href="#"><i class="fas fa-search mx-3"></i></a>
      </ul>
    </nav>
  </header>
</template>

<script>
//Importo file js per la navbar
import navItems from "../data/navItems.js"

export default {
  name: 'Header',
  data () {
    return {
      items: navItems
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../styles/generals.scss";

header {
  height: 100px;
  // background-color: red;

  ul {
    font-weight: 800;
    font-size: 12px;
    color: $gray;
    
    .active {
      color: $froly;
      border-bottom: 3px solid $froly;
    }

    li {
      a {
        color: $gray;
        &:hover {
          color: $froly;
          border-bottom: 3px solid $froly;          
        }
      }
    }
    a {
      color: $gray;
      &:hover {
        color: $froly;
      }
    }
  }
}
</style>
