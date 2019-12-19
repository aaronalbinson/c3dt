<template>
  <div id="app">
    <Card
      SubHeaderText="Sub-heading title"
      MainHeaderText="Main title sits here"
      ParagraphText="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam non urna eu augue maximus aliquam. Pellentesque sit amet lobortis sapien. Nullam maximus nibh id maximus vestibulum. Donec sit amet fringilla tellus, vel ultrices justo. Phasellus ornare turpis quis augue maximus mattis augue."
      CallToActionText="Call to action"
      CallToActionLink="https://google.com"
    />
    <C3Carousel />
    <AgileCarousel />
  </div>
</template>

<script>
import C3Carousel from "./components/C3Carousel/C3Carousel.vue";
import AgileCarousel from "./components/C3Carousel/AgileCarousel.vue";
import Card from "./components/Card/Card.vue";

export default {
  name: "app",
  components: {
    C3Carousel,
    Card,
    AgileCarousel
  }
};
</script>

<style>
body {
  margin: 0;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  max-width: 1500px;
  margin-top: 50px;
  margin-left: auto;
  margin-right: auto;
}
</style>
