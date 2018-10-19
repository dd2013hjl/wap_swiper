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
    <swiper :options="swiperOption" ref="mySwiper" id="mySwiper">
      <swiper-slide>
        <!-- <div style=" width: 100%;height: 100%;background: url(https://cache2.vphotos.cn/bkwft01/upload/photoAlbum/paster/4362571b50164948b7659f3e80d5983e.jpeg)no-repeat;background-size: cover;"></div> -->
        <img src="http://img.pailixiang.com/album/pailixiang/a152329377/24560519.jpg%40!lphoto" alt="" srcset="">
      </swiper-slide>
      <swiper-slide>
        <img src="http://img.pailixiang.com/album/pailixiang/a153909278/34889877.jpg%40!sphoto" alt="" srcset="">
      </swiper-slide>
      <swiper-slide>
        <img src="http://img.pailixiang.com/album/pailixiang/a152329377/24591356.jpg%40!lphoto" alt="" srcset="">
      </swiper-slide>
      <swiper-slide>
        <img src="https://cache2.vphotos.cn/bkwft01/upload/photoAlbum/paster/4362571b50164948b7659f3e80d5983e.jpeg" alt="" srcset="">
      </swiper-slide>
      <swiper-slide>
        <img src="https://cache2.vphotos.cn/bkwft01/upload/photoAlbum/paster/4362571b50164948b7659f3e80d5983e.jpeg" alt="" srcset="">
      </swiper-slide>
      <div class="swiper-button-prev" slot="button-prev"></div>
      <div class="swiper-button-next" slot="button-next"></div>
    </swiper>
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
<<<<<<< HEAD
  z-index: 1;
}
.swiper-container {
  width: 600px;
  height: 300px;
}
.swiper-slide {
  width: 100%;
  height: 400px;
=======
  z-index: 2;
  background: #000;
  display: flex;
  align-items: center;
  justify-content: center;
}
.swiper-wrapper{
  align-items: center!important;
  justify-content: center!important;
}
.swiper-slide{
  overflow: hidden;
}
.swiper-slide img{
  width: 100%;
>>>>>>> efd484b59fcf8485e7151cbd763581b75601d57d
}
</style>
