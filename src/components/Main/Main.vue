<template>
  <section class="main">
    <Info />
    <Diagram />
  </section>
</template>

<script>
import Info from "./Info/Info"
import Diagram from "./Diagram/Diagram"

export default {
  name: "Main",
  components: {
    Info,
    Diagram
  }
}
</script>

<style lang="scss" scoped>
  .main {
    max-width: 1309px;

    margin: 0 auto;
    padding-top: 33px; 
  }
</style>