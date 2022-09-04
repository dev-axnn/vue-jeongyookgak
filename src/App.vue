<template>
  <ModalView/>
  <MenuView/>
  <div class="wrap">
    <HeaderView/>
    <VisualView/>
    <EventView/>
  </div>
</template>

<script>
  import { onMounted } from 'vue';
  import $ from 'jquery';

  import ModalView from '@/components/ModalView.vue';
  import MenuView from '@/components/MenuView.vue';
  import HeaderView from '@/components/HeaderView.vue';
  import VisualView from '@/components/VisualView.vue';
  import EventView from '@/components/EventView.vue';

  export default {
    components: { 
      ModalView,
      MenuView,
      HeaderView,
      VisualView,
      EventView
    },

    setup(){
      onMounted(() => {
        // 스크롤시 header 고정
        let header = $('.header');
        let wrap = $('.wrap');
        // 사라지는 시점 px 값 = banner의 높이값 px
        let fixY = $('.top-banner').height();
        $(window).scroll(function(){
          // 스크롤바의 세로상단 px 값
          let temp = $(window).scrollTop();
          // 60 은 topbanner 의 높이값 px
          if(temp > fixY) {
            header.addClass('header-fix');
            wrap.addClass('wrap-fix');
          }else{
            header.removeClass('header-fix');
            wrap.removeClass('wrap-fix');
          }
        });

        // 팝업닫기
        let topBanner = $('.top-banner');
        let topBnClose = $('.top-bn-close');
        topBnClose.click(function(){
          fixY = 0;
          topBanner.slideUp(300);
        });
      });

      return{};
    }
}
</script>

<style>
  @charset 'utf-8';
  @import url('//spoqa.github.io/spoqa-han-sans/css/SpoqaHanSans-kr.css');

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    /* outline-style: none; */
  }

  a {
    color: #000;
    text-decoration: none;
  }

  ul,
  li {
    list-style: none;
  }

  img {
    vertical-align: middle;
    border: 0;
  }

  html {
    font-size: 16px;
  }

  body {
    font-family: 'Spoqa Han Sans', Arial, "Helvetica Neue", Helvetica, sans-serif;
    font-weight: 400;
    font-size: 12px;
    line-height: 1.0;
    letter-spacing: -0.32px;
  }

  /* ==== common ==== */
  .inner {
    position: relative;
    display: block;
    width: 100%;
    max-width: 1184px;
    margin: 0 auto;
  }

  .clearfix::after {
    content: '';
    position: relative;
    display: block;
    width: 100%;
    clear: both;
  }
  /* ==== //common ==== */
</style>