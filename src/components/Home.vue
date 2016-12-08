<template>
  <div class="home">
    <swiper class="my-swiper" :options="swiperOption">
      <swiper-slide v-for="i in arr">Slide {{i}}</swiper-slide>
      <div class="swiper-button-prev" slot="button-prev"></div>
      <div class="swiper-button-next" slot="button-next"></div>
    </swiper>
  </div>
</template>
<script>
import { swiper, swiperSlide, swiperPlugins } from 'vue-awesome-swiper'
export default {
  name: 'home',
  created: function() {
    let vm = this
    setTimeout(function() {
          vm.arr.push(4);
          vm.arr.push(5);
          vm.arr.push(6);
    }, 5000);
  },
  data() {
    return {
      arr:[1,2,3],
      swiperOption: {
          nextButton: '.swiper-button-next',
          prevButton: '.swiper-button-prev',
          slidesPerView: 1,
          spaceBetween: 30,
          loop: true
      }
    }
  },
  methods: {
  },
  components: {
    swiper,
    swiperSlide
  }
}
</script>
<style scoped>
.my-swiper {
  text-align: center;
  width: 50%;
  margin: 0 auto;
}
</style>