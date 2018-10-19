 <template>
  <div>
    <swiper :options="swiperOption" ref="mySwiper" id="mySwiper">
      <swiper-slide>
        <img src="https://cache2.vphotos.cn/bkwft01/upload/photoAlbum/paster/4362571b50164948b7659f3e80d5983e.jpeg" alt="" srcset="">
      </swiper-slide>
      <swiper-slide>
        <img src="https://cache2.vphotos.cn/bkwft01/upload/photoAlbum/paster/4362571b50164948b7659f3e80d5983e.jpeg" alt="" srcset="">
      </swiper-slide>
      <swiper-slide>
        <img src="https://cache2.vphotos.cn/bkwft01/upload/photoAlbum/paster/4362571b50164948b7659f3e80d5983e.jpeg" alt="" srcset="">
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
#mySwiper {
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  z-index: 2;
}
</style>
