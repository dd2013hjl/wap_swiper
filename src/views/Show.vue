 <template>
  <div id="wrap">
    <div class="swiper-container">
      <div class="swiper-wrapper">
        <div class="swiper-slide" v-for="item in imgList" :key="item">
          <img :src="item">
        </div>
      </div>
    </div>
    <div class="thumbs-container">
      <div class="swiper-wrapper">
        <div class="swiper-slide" v-for="item in imgList" :key="item">
          <img :src="item">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Swiper from 'swiper'

export default {
  data () {
    return {
      imgList: [
        require('assets/image/pum/1.jpg'),
        require('assets/image/pum/2.jpg'),
        require('assets/image/pum/3.jpg'),
        require('assets/image/pum/4.jpg'),
        require('assets/image/pum/5.jpg'),
        require('assets/image/pum/6.jpg'),
        require('assets/image/pum/7.jpg'),
        require('assets/image/pum/8.jpg')
      ]
    }
  },
  mounted () {
    const thumbSwiper = new Swiper('.thumbs-container', {
      spaceBetween: 10,
      slidesPerView: 4,
      watchSlidesVisibility: true
    })
    const swiper = new Swiper('.swiper-container', {
      spaceBetween: 10,
      loop: true,
      thumbs: {
        swiper: thumbSwiper
      }
    })
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
}
.swiper-container {
  width: 600px;
  height: 300px;
}
.swiper-slide {
  width: 100%;
  height: 400px;
}
</style>
