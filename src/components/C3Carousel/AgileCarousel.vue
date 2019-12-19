<template>
  <div>
    <p>{{ currentSlideNumber }}</p>
    <button @click="$refs.carousel.goToNext()">My custom button</button>
    <agile @afterChange="showCurrentSlide()" ref="carousel" class="AgileCarousel" :fade="true">
      <div>
        <div class="c3carouselSlide">
          <div class="c3carouselSlideImage">
            <img alt="Headphones and phone" src="@/assets/01.png" />
          </div>
        </div>
      </div>
      <div>
        <div class="c3carouselSlide">
          <div class="c3carouselSlideImage">
            <img alt="Desks with lamps" src="@/assets/02.png" />
          </div>
        </div>
      </div>
      <div>
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
      </div>
      <div v-if="isMobile()">
        <div class="c3carouselSlide">
          <div class="c3carouselSlideImage">
            <img alt="Robot" src="@/assets/04.png" />
          </div>
        </div>
      </div>
    </agile>
  </div>
</template>

<script>
import { VueAgile } from "vue-agile";

export default {
  name: "C3Carousel",
  components: {
    agile: VueAgile
  },
  data() {
    return {
      currentSlideNumber: 0
    };
  },
  methods: {
    isMobile() {
      if (window.innerWidth <= 700) {
        return true;
      } else {
        return false;
      }
    },
    showCurrentSlide() {
      /* eslint-disable no-console */
      var currentSlide = this.$refs.carousel.getCurrentSlide();
      this.currentSlideNumber = currentSlide;
      console.log(currentSlide);
    }
  }
};
</script>

<style>
.c3carousel {
  margin-bottom: 30px;
}
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
.c3carousel .VueCarousel-pagination .VueCarousel-dot-container button {
  min-width: 40px;
  max-height: 4px;
  border-radius: 0;
}

@media only screen and (min-width: 700px) {
  .c3carousel img {
    width: 100%;
    height: auto;
    object-fit: none;
    object-position: top;
  }
  .c3carouselSlideImage {
    height: auto;
  }
  .c3carousel .VueCarousel-pagination {
    text-align: right;
  }
}
</style>
