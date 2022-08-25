<template>
  <!-- visual -->
  <section class="visual">
  </section>
  <!-- //visual -->
</template>

<script>
export default {

}
</script>

<style scoped>
  /* visual */
  .visual {
    position: relative;
    display: block;
    height: 560px;
    background: url('@/assets/images/main_firstgift_logout.29ecc8b.png') no-repeat center;
    background-size: cover;
    cursor: pointer;
    transition: all 0.3s;
  }

  @media screen and (max-width: 1200px) {
    .visual {
      height: 500px;
      background: url('@/assets//images/main_firstgift_logout.29ecc8b_m.png') no-repeat center left;
      background-size: cover;
    }
  }

  @media screen and (max-width: 900px) {
    .visual {
      height: 400px;
    }
  }
</style>