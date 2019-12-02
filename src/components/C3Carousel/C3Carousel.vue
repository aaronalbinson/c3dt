<template>
  <carousel class="c3carousel" :scrollPerPage="true" :perPageCustom="[[0, 1], [700, 2], [1000, 3]]">
    <slide>
      <div class="c3carouselSlide">
        <div class="c3carouselSlideImage">
          <img alt="Headphones and phone" src="@/assets/01.png" />
        </div>
      </div>
    </slide>
    <slide>
      <div class="c3carouselSlide">
        <div class="c3carouselSlideImage">
          <img alt="Desks with lamps" src="@/assets/02.png" />
        </div>
      </div>
    </slide>
    <slide>
      <div class="c3carouselSlide">
        <div>
          <div class="c3carouselSlideImage">
            <img alt="Smart watch" src="@/assets/03.png" />
          </div>
        </div>
        <div v-if="!isMobile()">
          <div class="c3carouselSlideImage">
            <img alt="Robot" src="@/assets/04.png" />
          </div>
        </div>
      </div>
    </slide>
    <slide v-if="isMobile()">
      <div class="c3carouselSlide">
        <div class="c3carouselSlideImage">
          <img alt="Robot" src="@/assets/04.png" />
        </div>
      </div>
    </slide>
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

<style>
.c3carousel img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
}
.c3carouselSlide {
  padding: 0 20px;
  display: flex;
  flex-direction: column;
  height: 100%;
  justify-content: space-between;
}
.c3carouselSlideImage {
  height: calc(100vw - 40px);
  
}
.c3carousel .VueCarousel-pagination {
  margin-bottom: 30px;
}
.c3carousel .VueCarousel-pagination .VueCarousel-dot-container button{
  min-width: 40px;
  max-height: 4px;
  border-radius: 0;
}
</style>
