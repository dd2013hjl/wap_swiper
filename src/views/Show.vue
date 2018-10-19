<template>
  <div id="wrap">
    <div class="swiper-container">
      <div class="swiper-wrapper">
      </div>
    </div>
    <div class="thumbs-container">
      <div class="swiper-wrapper">
      </div>
    </div>
  </div>
</template>

<script>
import Swiper from 'swiper'
import axios from 'axios'

let imgSwiper = null
let thumbSwiper = null

export default {
  data () {
    return {
      imgList: []
    }
  },
  created () {
    this.getPhoList()
  },
  methods: {
    async getPhoList () {
      let list = await axios.get('/api/pho')
      this.imgList = list.data.list

      thumbSwiper = this.initThumbSwiper(0, this.imgList)
      imgSwiper = this.initSwiper(0, this.imgList)
    },
    initThumbSwiper (index, list) {
      const thumbSwiper = new Swiper('.thumbs-container', {
        slidesPerView: 8, // 设置slider容器能够同时显示的slides数量
        spaceBetween: 4, // 在slide之间设置距离
        initialSlide: index,
        centeredSlides: true,
        slideToClickedSlide: true,
        watchSlidesVisibility: true,
        virtual: {
          renderSlide: (item, index) => {
            var tpl = `<div class="swiper-slide"><div style="background:url('${item.thumb}')  no-repeat"></div></div>`
            return tpl
          },
          slides: list
        }
      })
      return thumbSwiper
    },
    initSwiper (index, list) {
      const imgSwiper = new Swiper('.swiper-container', {
        observer: true,
        observeParents: true,
        centeredSlides: true,
        spaceBetween: 20,
        initialSlide: index,
        virtual: {
          renderSlide: (item, index) => {
            var tpl = `<div class="swiper-slide"><div style="background:url('${item.src}') no-repeat"></div></div>`
            return tpl
          },
          slides: list
        },
        thumbs: {
          swiper: thumbSwiper
        }
      })
      return imgSwiper
    }
  }
}
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
.thumbs-container .swiper-slide-active {
  box-sizing: border-box;
  border: 1px solid #fff;
}
</style>
