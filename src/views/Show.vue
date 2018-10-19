 <template>
  <div id="wrap">
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
export default {
  data () {
    return {
      swiperOption: {
        loop: true,
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
        }
      }
    }
  },
  computed: {
    swiper () {
      return this.$refs.mySwiper.swiper
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
}
</style>
