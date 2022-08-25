<template>
  <!-- top banner -->
  <div class="top-banner">
    <div class="inner">
      <a href="#">추천상품</a>
      <button class="top-bn-close">닫기</button>
    </div>
  </div>
  <!-- //top banner -->

  <!-- header -->
  <header class="header">
    <div class="inner">
      <div>
        <a href="#" class="logo">정육각</a>
        <ul class="gnb clearfix">
          <li><a href="#">쇼핑하기</a></li>
          <li><a href="#">배송하기</a></li>
          <li><a href="#">이벤트</a></li>
        </ul>
      </div>
      <div>
        <ul class="unb clearfix">
          <li><a href="#">공지사항</a></li>
          <li><a href="#">고객센터</a></li>
          <li class="unb-line"></li>
          <li><a href="#">로그인</a></li>
          <li><a href="#">회원가입</a></li>
        </ul>
      </div>
      <a href="#" class="header-cart">장바구니</a>
      <a href="#" class="header-menu">전체메뉴</a>
    </div>
  </header>
  <!-- //header -->
</template>

<script>
  export default {
    
  }
</script>

<style scoped>
  /* header */
  .top-banner {
    position: relative;
    display: block; 
    height: 60px;
    background: radial-gradient(circle at 50% 527%, #ff896a, #e23000);
  }

  .top-banner .inner a {
    position: relative;
    display: block;
    height: 60px;
    font-size: 0;
    background: url('@/assets/images/img_firstorder_gift.png') no-repeat 50% 0%;
    background-size: contain;
  }

  .top-bn-close {
    position: absolute;
    right: 10px;
    top: 50%;
    transform: translateY(-50%);
    width: 45px;
    height: 30px;
    font-size: 0;
    opacity: 0;
    border: 0;
    background: none;
    cursor: pointer;
  }

  .header {
    position: relative;
    display: block;
    height: 96px;
    background: #000;
    z-index: 9999;
  }

  .header .inner {
    position: relative;
    display: block;
    height: 100%;
  }

  .logo {
    position: absolute;
    left: 0;
    display: block;
    width: 129px;
    height: 96px;
    font-size: 0;
    background: url('@/assets/images/logo.svg') no-repeat center;
    background-size: contain;
  }

  .gnb {
    position: absolute;
    left: calc(150px + 2%);
    top: 52%;
    transform: translateY(-50%);
    display: block;
  }

  .gnb li {
    float: left;
    margin-right: 20px;
  }

  .gnb li a {
    display: block;
    font-size: 18px;
    color: #fff;
  }

  .unb {
    position: absolute;
    right: 11%;
    top: 53%;
    transform: translateY(-50%);
    display: block;
  }

  .unb li {
    position: relative;
    display: block;
    float: left;
  }

  .unb li a {
    position: relative;
    display: block;
    color: #fff;
    font-size: 14px;
    font-weight: 400;
    margin-left: 12px;
  }

  .unb-line {
    width: 1px;
    height: 14px;
    background: #fff;
    margin-left: 20px;
    margin-right: 8px;
  }

  .header-cart {
    position: absolute;
    right: 56px;
    top: 50%;
    transform: translateY(-50%);
    display: block;
    width: 48px;
    height: 48px;
    font-size: 0;
    background: url('@/assets/images/icon-cart.svg') no-repeat center;
    background-size: contain;
    float: right;
  }

  .header-menu {
    position: absolute;
    right: 0;
    top: 50%;
    transform: translateY(-50%);
    display: block;
    width: 48px;
    height: 48px;
    font-size: 0;
    background: url('@/assets/images/icon-menu.svg') no-repeat center;
    background-size: contain;
    float: right;
  }

  .header-fix {
    position: fixed;
    left: 0;
    top: 0;
    width: 100%;
  }

  .wrap-fix {
    padding-top: 96px;
  }

  @media screen and (max-width: 1200px) {
    .top-banner {
      display: none;
    }

    .header {
      height: 70px;
      background: #000;
      z-index: 9999;
    }

    .logo {
      left: 2%;
      top: 50%;
      transform: translateY(-50%);
      height: 43px;
    }

    .unb {
      right: 125px;
    }

    .header-cart {
      right: calc(2% + 45px);
      width: 43px;
      height: 43px;
    }
    
    .header-menu {
      right: 2%;
      width: 43px;
      height: 43px;
    }
  }


  @media screen and (max-width: 900px) {
    .logo {
      left: 2%;
      top: 50%;
      transform: translateY(-50%);
      height: 40px;
    }

    .gnb {
      left: calc(140px + 2%);
    }

    .unb {
      display: none;
    }

    .gnb li a {
      display: block;
      font-size: 16px;
      color: #fff;
    }

    .header-cart {
      width: 40px;
      height: 40px;
    }
    
    .header-menu {
      width: 40px;
      height: 40px;
    }
  }
</style>