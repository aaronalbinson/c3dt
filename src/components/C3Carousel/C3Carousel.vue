<template>
  <carousel :scrollPerPage="true" :perPageCustom="[[0, 1], [700, 2], [1000, 3]]">

    <slide>Slide 1 Content</slide>
    <slide>Slide 2 Content</slide>
    <slide>
      <div>Slide 3 Content</div>
      <div v-if="!isMobile()">Slide 4 Content</div>
    </slide>
    <slide v-if="isMobile()">Slide 4 Content</slide>
  </carousel>
</template>

<script>
import { Carousel, Slide } from "vue-carousel";

export default {
  name: "C3Carousel",
  props: {
    msg: String
  },
  components: {
    Carousel,
    Slide
  },
  methods: {
    isMobile() {
      if (window.innerWidth <= 700) {
        return true;
      } else {
        return false;
      }
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
