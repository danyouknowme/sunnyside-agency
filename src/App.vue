<template>
  <div id="app">
    <Navbar :isScrolled="isScrolled"/>
    <Header />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue"
import Header from "./components/Header.vue"

export default {
  name: 'App',
  components: {
    Navbar,
    Header,
  },
  data() {
    return {
      windowTop: 0,
      isScrolled: false,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.onScroll);
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.onScroll);
  },
  methods: {
    onScroll(e) {
      this.windowTop = e.target.documentElement.scrollTop;
      (this.windowTop === 0 ? this.isScrolled = false : this.isScrolled = true);
    },
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Barlow:wght@600&family=Fraunces:wght@700;900&display=swap');

html, body {
  margin: 0 !important;
  padding: 0 !important;
  overflow-x: hidden;
}

#app {
  font-family: 'Barlow', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  font-size: 18px;
}
</style>
