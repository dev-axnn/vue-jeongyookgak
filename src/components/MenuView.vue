<template>
  <!-- menu -->
  <div class="menu">
    <h3>메뉴</h3>
    <a href="#" class="mn-cart">장바구니</a>
    <a href="#" class="mn-close">닫기</a>
    <div>
      <h4>쇼핑하기</h4>
      <ul class="mn-category clearfix">
        <li><img :src="require('@/assets/images/ct-pig.svg')" alt="돼지"><p>돼지</p></li>
        <li><img :src="require('@/assets/images/ct-cow.svg')" alt="소"><p>소</p></li>
        <li><img :src="require('@/assets/images/ct-chicken.svg')" alt="닭"><p>닭</p></li>
        <li><img :src="require('@/assets/images/ct-fish.svg')" alt="수산"><p>수산</p></li>
        <li><img :src="require('@/assets/images/ct-mealkit.svg')" alt="밀키트"><p>밀키트</p></li>
        <li><img :src="require('@/assets/images/ct-milk.svg')" alt="우유"><p>우유</p></li>
        <li><img :src="require('@/assets/images/ct-egg.svg')" alt="달걀"><p>달걀</p></li>
        <li><img :src="require('@/assets/images/ct-babymeal.svg')" alt="이유식"><p>이유식</p></li>
      </ul>
    </div>
    <hr>
    <div class="mn-etc">
      <ul>
        <li><a href="#">브랜드스토리</a></li>
        <li><a href="#">이용가이드</a></li>
        <li><a href="#">공지사항</a></li>
        <li><a href="#">고객센터</a></li>
        <li><a href="#">마이페이지</a></li>
      </ul>
    </div>
  </div>
</template>

<script>
  import { onMounted } from 'vue';
  import $ from 'jquery';

  export default {
    setup(){
      onMounted(() => {
        // 메뉴열기
        let headerMenu = $('.header-menu');
        let menu = $('.menu');
        headerMenu.click(function(event){
          event.preventDefault();
          menu.addClass('menu-open');
        });
  
        // 메뉴닫기
        let mnClose = $('.mn-close');
        mnClose.click(function(event){
          event.preventDefault();
          menu.removeClass('menu-open');
        });
      });

      return{};
    }
  }
</script>

<style scoped>
  /* menu */
  .menu {
    position: fixed;
    right: -600px;
    top: 0;
    display: block;
    width: 480px;
    height: 100vw;
    background: #fff;
    box-shadow: 0 0 30px 0 rgba(0, 0, 0, 0.1);
    z-index: 9999;
    transition: right 0.5s;
  }

  .menu-open {
    position: fixed;
    right: 0;
    top: 0;
  }

  .menu h3 {
    position: relative;
    display: block;
    font-size: 24px;
    line-height: 48px;
    margin: 15px 16px 0 25px;
  }

  .mn-cart {
    position: absolute;
    right: 73px;
    top: 15px;
    display: block;
    width: 48px;
    height: 48px;
    font-size: 0;
    background: url('@/assets/images/mn-cart.svg') no-repeat center;
    background-size: contain;
  }

  .mn-close {
    position: absolute;
    right: 16px;
    top: 15px;
    display: block;
    width: 48px;
    height: 48px;
    font-size: 0;
    background: url('@/assets/images/mn-close.svg') no-repeat center;
    background-size: contain;
  }

  .menu h4 {
    position: relative;
    margin: 38px 16px 0 25px;
    font-size: 18px;
    font-weight: 400;
    margin-bottom: 10px;
  }

  .mn-category {
    position: relative;
    display: block;
    margin: 5px 0 0 8px;
  }

  .mn-category li {
    position: relative;
    display: block;
    width: 104px;
    height: 128px;
    text-align: center;
    border-radius: 8px;
    cursor: pointer;
    margin-right: 16px;
    padding-top: 25px;
    padding-bottom: 25px;
    float: left;
  }

  .mn-category li:hover {
    background: #f6f6f6;
  }

  .mn-category li:nth-child(4n) {
    margin-right: 0;
  }

  .mn-category li img {
    margin-bottom: 8px;
    width: 48px;
    height: 48px;
  }

  .mn-category li p {
    position: relative;
    display: block;
    font-size: 18px;
    line-height: 28px;
  }

  .menu hr {
    margin: 23px 0;
    border: 0.5px solid #e0e0e0;
  }

  .mn-etc {
    margin: 32px 16px 0 25px;
  }

  .mn-etc ul {
    font-size: 18px;
    font-weight: 800;
    line-height: 27px;
    letter-spacing: -0.1px;
  }

  .mn-etc ul li {
    margin-bottom: 21px;
    cursor: pointer;
  }

  .mn-etc ul li:last-child {
    margin-top: 40px;
  }
</style>