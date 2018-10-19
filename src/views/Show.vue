
<template>
  <div id="wrap">
    <div class="swiper-container">
      <div class="swiper-wrapper">
        <div class="swiper-slide" v-for="(item,index) in imgList" :key="index">
          <img :src="item">
        </div>
      </div>
    </div>
    <div class="thumbs-container">
      <div class="swiper-wrapper">
        <div class="swiper-slide" v-for="(item,index) in imgList" :key="index">
          <!-- <img :src="item"> -->
          <div class="imgitem" :style="{backgroundImage: 'url('+item+')'}"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Swiper from "swiper";

export default {
  data() {
    return {
      imgList: [
        require("assets/image/swiperimg.jpg"),
        require("assets/image/timg.jpg"),
        require("assets/image/timg.jpg"),
        require("assets/image/timg.jpg"),
        require("assets/image/timg.jpg"),
        require("assets/image/timg.jpg"),
        require("assets/image/timg.jpg"),
        require("assets/image/timg.jpg")
      ]
    };
  },

  mounted() {
    const thumbSwiper = new Swiper(".thumbs-container", {
      spaceBetween: 10,
      slidesPerView: 4,
      watchSlidesVisibility: true
    });

    const swiper = new Swiper(".swiper-container", {
      spaceBetween: 10,
      loop: true,
      thumbs: {
        swiper: thumbSwiper
      }
    });
  }
};
</script>

<style scoped>
#wrap {
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  z-index: 1;
  background: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #000;
}

.swiper-container {
  display: flex;
  align-items: center;
}

.swiper-wrapper {
  align-items: center;
}

.swiper-slide {
  overflow: hidden;
}

.swiper-slide img {
  width: 100%;
}

.thumbs-container {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 20px;
  z-index: 3;
}

.thumbs-container .imgitem {
  width: 80px;
  height: 60px;
  background-size: cover;
  background-position: 50% 50%;
  background-repeat: no-repeat;
}

.thumbs-container .swiper-slide,
.thumbs-container .swiper-slide-visible,
.thumbs-container .swiper-slide-active {
  margin-right: 5px !important;
  width: 80px !important;
}
.thumbs-container .swiper-slide-active{
  box-sizing: border-box;
  border: 1px solid #fff;
}
</style>