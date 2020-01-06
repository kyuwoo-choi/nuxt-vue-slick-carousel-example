<template>
  <div class="carousel-wrapper">
    <VueSlickCarousel v-bind="slickOptions">
      <div v-for="i in 5" :key="i" class="img-warpper">
        <img :src="`https://picsum.photos/200/100?random=${i}`" />
      </div>
    </VueSlickCarousel>
  </div>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'

export default {
  components: {
    VueSlickCarousel
  },
  data() {
    return {
      slickOptions: {
        slidesToShow: 3,
        arrows: false,
        dots: true,
      }
    }
  }
}
</script>

<style>
.carousel-wrapper {
  padding: 40px;
  height: 150px;
}
.img-warpper img {
  margin: auto;
  width: 200px;
  height: 100px;
  background-image: linear-gradient(gray 100%, transparent 0);
}
</style>
