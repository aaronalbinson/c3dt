<template>
  <div id="app">
    <SubHeader SubHeaderText="Sub-heading title"/>
    <MainHeader MainHeaderText="Main title sits here"/>
    <Paragraph ParagraphText="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam non urna eu augue maximus aliquam. Pellentesque sit amet lobortis sapien. Nullam maximus nibh id maximus vestibulum. Donec sit amet fringilla tellus, vel ultrices justo. Phasellus ornare turpis quis augue maximus mattis augue."/>
    <CallToAction CallToActionText="Call to action" CallToActionLink="https://google.com"/>
    <C3Carousel/>
  </div>
</template>

<script>
import C3Carousel from './components/C3Carousel/C3Carousel.vue'
import SubHeader from './components/Headers/SubHeader.vue'
import MainHeader from './components/Headers/MainHeader.vue'
import Paragraph from './components/Paragraph/Paragraph.vue'
import CallToAction from './components/CallToAction/CallToAction.vue'

export default {
  name: 'app',
  components: {
    C3Carousel,
    SubHeader,
    MainHeader,
    Paragraph,
    CallToAction
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
}
</style>
