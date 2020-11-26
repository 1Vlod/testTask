<template>
  <div id="app">
    <Header/>
    <Main/>
    <Footer/>
  </div>
</template>

<script>
import Header from "@/components/Header"
import Main from "@/components/Main/Main"
import Footer from "@/components/Footer"

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer
  }
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;900&display=swap');

html, body {
  margin: 0;
  box-sizing: border-box;
}

#app {
  font-family: Roboto, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
