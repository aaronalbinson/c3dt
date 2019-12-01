<template>
  <div id="app">
    <SubHeader SubHeaderText="Sub-heading title"/>
    <MainHeader MainHeaderText="Main title sits here"/>
    <C3Carousel/>
  </div>
</template>

<script>
import C3Carousel from './components/C3Carousel/C3Carousel.vue'
import SubHeader from './components/Headers/SubHeader.vue'
import MainHeader from './components/Headers/MainHeader.vue'

export default {
  name: 'app',
  components: {
    C3Carousel,
    SubHeader,
    MainHeader
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
}
</style>
