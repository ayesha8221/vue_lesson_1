<template>
  <!-- <nav>
import FooterComp from './components/FooterComp.vue';
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <router-view/> -->
  <NavbarComp/>
  <router-view/>
  <FooterComp/>
</template>
<script>
import NavbarComp from './components/NavbarComp.vue';
import FooterComp from './components/FooterComp.vue';

export default {

  components: { NavbarComp, FooterComp }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #365e86;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #4e6f91;
}

nav a.router-link-exact-active {
  color: #4bb284;
  display: flex;
  justify-content: start;
  /* align-items: flex-start; */
}
</style>
