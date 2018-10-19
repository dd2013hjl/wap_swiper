<template>
  <div id="wrap">
    <img src="http://www.pailixiang.com/Themes/album/images/close2.png" class="close_btn" />
    <div class="swiper-container">
      <div class="swiper-wrapper">
      </div>
    </div>

    <div class="footer">
      <div class="thumbs-container">
        <div class="swiper-wrapper">
        </div>
      </div>
      <div class="footer_info">
        <span>摄影师：董某某</span>
        <div class="ico">
          <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABwAAAAcCAYAAAByDd+UAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyFpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuNS1jMDE0IDc5LjE1MTQ4MSwgMjAxMy8wMy8xMy0xMjowOToxNSAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENDIChXaW5kb3dzKSIgeG1wTU06SW5zdGFuY2VJRD0ieG1wLmlpZDoxQUNCRTQwREMyMzUxMUU4OEIyQUZEOEJCRjcyNjc4NiIgeG1wTU06RG9jdW1lbnRJRD0ieG1wLmRpZDoxQUNCRTQwRUMyMzUxMUU4OEIyQUZEOEJCRjcyNjc4NiI+IDx4bXBNTTpEZXJpdmVkRnJvbSBzdFJlZjppbnN0YW5jZUlEPSJ4bXAuaWlkOjFBQ0JFNDBCQzIzNTExRTg4QjJBRkQ4QkJGNzI2Nzg2IiBzdFJlZjpkb2N1bWVudElEPSJ4bXAuZGlkOjFBQ0JFNDBDQzIzNTExRTg4QjJBRkQ4QkJGNzI2Nzg2Ii8+IDwvcmRmOkRlc2NyaXB0aW9uPiA8L3JkZjpSREY+IDwveDp4bXBtZXRhPiA8P3hwYWNrZXQgZW5kPSJyIj8+MkNKuwAAAK5JREFUeNrkVVsOgCAMc4QDeP9TeoMqiSghPDYCE3WJiR81tbRlBGDRHHs8qoxmUR4bvNNgLjyu8JZK/cTGoVRXOCehOxZuX2tYk/loRTA1f04Sj0XKu2JoGCFAa5VMJqUbCaLqoFz8HD1kKKKST+9XGCSXJLeMWGGP3VnsYXzTV8rOwtuGwFxH2aKYUn6kKuVh3HomfgYihdKV5fH/W092VPynVIjPekiahLsAAwAsnmwc0SC20wAAAABJRU5ErkJggg==" />
          <span>原图1.9M</span>
        </div>
        <div class="ico">
          <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABwAAAAcCAYAAAByDd+UAAAAAXNSR0IArs4c6QAAAj5JREFUSA3dlj1rFFEUhncTiIUxaiOkUAISBAsLUfwKiWKtqJWNNtpqqz9AQTSFiKAQiGUKIf4CNUIKBVtjJagQrSIWigY/1ueZ3HthZzeXdWeqvPDsnHvPOe+ZYXZ2ttHY6GqWL7DVah1g7zycgN3wDb7CU5hvNpsvOCZRP8XiHJyE7bAZ3sECzFH/mmOnaByBB/AHclokuT9gnJNeD2GkbSIbQ7AA6ifchgnwJHbAQbgBn0BpFE/MPXPWWLsF7NVDL6X3UBrKYsZd9B7GU6IUkBuGW/ArYDxcKktLcuOgp5opEgRj8Bt+wN5UnQmoOyqZkpTSE/R2xliDjzug1s4gldYX6F1MYJYD442frG9EuxMzJsPARQcuh8Voe1l9K/xHw4xlB66Gxbo3v+po/P2yqdUBzFaC4Z6qxpn+6L3iwKVQ2NM3NGOaS0XvNw58FirP5Doq5qL3c+/hTvAZ+Qv7Khp3tOsZvJ2xqyggmAP1pKOj4gae84UzM5IVG17l95C4nBIVA/wuBU+9164uerJxISR9TCbifr9HPI5BfOQudvWhYBrUF+h7KL0O00NNdx3mJslBeGwV8gfXF+t/iZ6zoZdD4TWYNaBoAO5bjXzn3YRN2SaS1oDvRXuUHj52vYniaxCb3xKv+zoidwSWQNlzvbcppSoap+ADKI3ugf9ZChnDXYgn9pH4eEj3d8BgK8yCPwzqM1yFKxD/cph7BNv6m9KlC7ND8ArKcu9wl5Z6tjA/BS/BQafrcd1ILv8AkRb5s9U8IbwAAAAASUVORK5CYII=" />
          <span>点赞</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Swiper from "swiper";
import axios from "axios";

let imgSwiper = null;
let thumbSwiper = null;

export default {
  data() {
    return {
      imgList: [],
      imgStyle: `width:100%;height:auto`
    };
  },
  created() {
    this.getPhoList();
  },
  methods: {
    async getPhoList() {
      let list = await axios.get("/api/pho");
      this.imgList = list.data.list;

      thumbSwiper = this.initThumbSwiper(0, this.imgList);
      imgSwiper = this.initSwiper(0, this.imgList);
    },
    initThumbSwiper(index, list) {
      const thumbSwiper = new Swiper(".thumbs-container", {
        slidesPerView: 8, // 设置slider容器能够同时显示的slides数量
        spaceBetween: 4, // 在slide之间设置距离
        initialSlide: index,
        centeredSlides: true,
        slideToClickedSlide: true,
        watchSlidesVisibility: true,
        virtual: {
          renderSlide: (item, index) => {
            var tpl = `<div class="swiper-slide"><div style="background:url(${
              item.thumb
            }) no-repeat;height:40px;background-size:cover;"></div></div>`;
            return tpl;
          },
          slides: list
        }
      });
      return thumbSwiper;
    },
    initSwiper(index, list) {
      const imgSwiper = new Swiper(".swiper-container", {
        observer: true,
        observeParents: true,
        centeredSlides: true,
        spaceBetween: 20,
        initialSlide: index,
        virtual: {
          renderSlide: (item, index) => {
            var tpl = `<div class="swiper-slide"><img src='${
              item.src
            }' style="${this.imgStyle}"/></div>`;
            return tpl;
          },
          slides: list
        },
        thumbs: {
          swiper: thumbSwiper,
          slideThumbActiveClass: 'thumb_active',
        }
      });
      return imgSwiper;
    }
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
.close_btn {
  position: fixed;
  right: 10px;
  top: 10px;
  z-index: 100;
  width: 16px;
  height: 16px;
  padding: 10px;
  background: rgba(110, 113, 117, 0.5);
  border-radius: 50%;
  text-align: center;
  z-index: 2;
}
.swiper-container {
  display: flex;
  align-items: center;
  width: 100%;
}

.swiper-wrapper {
  align-items: center;
}
.footer {
  position: fixed;
  z-index: 100;
  bottom: 0;
  left: 0;
  overflow: hidden;
  width: 100%;
  height: auto;
  color: #fff;
}
.footer .thumbs-container {
  display: inline-block;
  width: 100%;
}
.footer .footer_info {
  padding: 20px 10px 10px;
  display: flex;
  align-items: center;
  background: #000;
  justify-content: space-between;
}
.footer .footer_info > span {
  flex-grow: 1;
}
.footer .footer_info .ico {
  flex-shrink: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  font-size: 10px;
  margin-left: 15px;
}
.footer .footer_info .ico img {
  width: 12px;
  height: 12px;
  margin-bottom: 4px;
}
.thumb_active{
  box-sizing: border-box;
  border: 1px solid #fff;
}
</style>
