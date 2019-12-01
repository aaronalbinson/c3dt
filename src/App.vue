<template>
  <div id="app">
    <SubHeader SubHeaderText="Sub-heading title"/>
    <C3Carousel/>
  </div>
</template>

<script>
import C3Carousel from './components/C3Carousel/C3Carousel.vue'
import SubHeader from './components/Headers/SubHeader.vue'

export default {
  name: 'app',
  components: {
    C3Carousel,
    SubHeader
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
