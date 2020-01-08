<template>
  <div class="carousel-wrapper">
    <VueSlickCarousel v-bind="slickOptions">
      <div v-for="i in 5" :key="i" class="img-wrapper">
        <img :src="`./${i}-200x100.jpg`" />
      </div>
    </VueSlickCarousel>
  </div>
</template>

<script>
export default {
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
}
.img-wrapper img {
  margin: auto;
  width: 200px;
  height: 100px;
  background-image: linear-gradient(gray 100%, transparent 0);
}
</style>
