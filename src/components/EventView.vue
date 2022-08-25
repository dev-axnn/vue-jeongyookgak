<template>
  <!-- event -->
    <section class="event">
      <div class="inner">
        <div class="swiper-container event-left">
          <div class="swiper-wrapper">
            <div class="swiper-slide">
              <a href="$"><img src="images/event-left-1.png" alt=""></a>
            </div>
            <div class="swiper-slide">
              <a href="$"><img src="images/event-left-2.png" alt=""></a>
            </div>
            <div class="swiper-slide">
              <a href="$"><img src="images/event-left-3.png" alt=""></a>
            </div>
            <div class="swiper-slide">
              <a href="$"><img src="images/event-left-4.png" alt=""></a>
            </div>
            <div class="swiper-slide">
              <a href="$"><img src="images/event-left-5.png" alt=""></a>
            </div>
            <div class="swiper-slide">
              <a href="$"><img src="images/event-left-6.png" alt=""></a>
            </div>
          </div>
          <div class="event-left-ctrl clearfix">
            <button class="event-left-prev"></button>
            <span class="event-left-pg"></span>
            <button class="event-left-next"></button>
          </div>
        </div>
        <div>
          <a href="#" class="event-right"></a>
        </div>
      </div>
    </section>
    <!-- //event -->
</template>

<script>
  import { onMounted } from 'vue';
  import $ from 'jquery';

  export default {
    setup(){
      onMounted(() => {
        // 이벤트슬라이드(swiper)
        new Swiper('.event-left', {
          loop: true,
          speed: 500,
          navigation: {
            prevEl: '.event-left-prev',
            nextEl: '.event-left-next'
          },
          pagination: {
            el: '.event-left-pg',
            type: 'fraction'
          }
        });
      });
      
      return{};
    }
  }
</script>

<style scoped>
  /* event */
  .event {
    position: relative;
    display: block;
    margin-top: 50px;
    margin-bottom: 80px;
    overflow: hidden;
  }

  .event-left {
    position: relative;
    display: block;
    width: calc(100% / 2);
    height: 18vw;
    max-height: 176px;
    float: left;
  }

  .event-left a {
    position: absolute;
    left: 0;
    top: 50%;
    transform: translateY(-50%);
    display: block;
  }
  .event-left a img{
    width: 100%;
    height: 30%;
  }

  .event-left-1 {
    background: url('../images/event-left-1.png') no-repeat center;
    background-size: cover;
  }
  .event-left-2 {
    background: url('../images/event-left-2.png') no-repeat center;
    background-size: cover;
  }
  .event-left-3 {
    background: url('../images/event-left-3.png') no-repeat center;
    background-size: cover;
  }
  .event-left-4 {
    background: url('../images/event-left-4.png') no-repeat center;
    background-size: cover;
  }
  .event-left-5 {
    background: url('../images/event-left-5.png') no-repeat center;
    background-size: cover;
  }
  .event-left-6 {
    background: url('../images/event-left-6.png') no-repeat center;
    background-size: cover;
  }

  .event-left-ctrl {
    position: absolute;
    left: 10px;
    bottom: 8px;
    display: block;
    width: 105px;
    height: 32px;
    border: 1px solid #eaeaea;
    background: #fff;
    z-index: 999;
  }

  .event-left-prev {
    width: 30%;
    height: 100%;
    background: url('../images/event-arrow.svg') no-repeat 50% 40%;
    background-size: 55%;
    transform: rotate(180deg);
    border: 0;
    float: left;
    cursor: pointer;
  }

  .event-left-pg {
    display: block;
    width: 40%;
    height: 30px;
    font-size: 13px;
    text-align: center;
    line-height: 30px;
    float: left;
  }

  .swiper-pagination-current {
    font-weight: 800;
  }

  .event-left-next {
    width: 30%;
    height: 100%;
    background: url('../images/event-arrow.svg') no-repeat center;
    background-size: 55%;
    opacity: .3;
    border: 0;
    float: left;
    cursor: pointer;
  }

  .event-right {
    position: relative;
    display: block;
    float: right;
    width: calc(100% / 2);
    height: 18vw;
    max-height: 176px;
    background: url('../images/freshplan.9fe4775.png') no-repeat center;
    background-size: contain;
  }

  @media screen and (max-width: 1300px) {
    .event {
      margin-top: 30px;
      margin-bottom: 80px;
    }

    .event-left {
      margin-left: 3%;
      width: calc(94% / 2);
    }

    .event-right {
      margin-right: 3%;
      width: calc(94% / 2);
    }
  }

  @media screen and (max-width: 1000px) {
    .event-left {
      width: 100%;
      height: 30vw;
      max-height: 300px;
      margin-bottom: 20px;
    }

    .event-left a {
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
      width: 90%;
    }

    .event-left-ctrl {
      left: 6%;
      bottom: 10%;
    }

    .event-left-pg {
      font-size: 13px;
      line-height: 30px;
    }

    .event-right {
      float: left;
      width: 90%;
      height: 30vw;
      max-height: 300px;
      background: url('../images/freshplan.9fe4775_m.png') no-repeat center;
      background-size: 89%;
      margin-left: 5%;
    }

    .event-right::before {
      content: '';
      position: absolute;
      bottom: 31.2vw;
      left: 50%;
      transform: translateX(-50%);
      width: 98%;
      height: 1px;
      background: #eaeaea;
    }
  }

  @media screen and (max-width: 800px) {
    .event-left-ctrl {
      width: 95px;
      height: 28px;
    }

    .event-left-pg {
      height: 28px;
      font-size: 12px;
      line-height: 28px;
    }
  }
</style>