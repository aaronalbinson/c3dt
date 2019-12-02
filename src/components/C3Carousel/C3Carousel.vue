<template>
  <carousel class="c3carousel" :scrollPerPage="true" :perPageCustom="[[0, 1], [700, 2], [1000, 3]]">

    <slide><img alt="Headphones and phone" src="@/assets/01.png"></slide>
    <slide><img alt="Desks with lamps" src="@/assets/02.png"></slide>
    <slide>
      <div><img alt="Smart watch" src="@/assets/03.png"></div>
      <div v-if="!isMobile()"><img alt="Robot" src="@/assets/04.png"></div>
    </slide>
    <slide v-if="isMobile()"><img alt="Robot" src="@/assets/04.png"></slide>
  </carousel>
</template>

<script>
import { Carousel, Slide } from "vue-carousel";

export default {
  name: "C3Carousel",
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
  .c3carousel img {
    width: 100%;
    height: auto;
  }
</style>
