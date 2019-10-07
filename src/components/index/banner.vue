<template>
  <div class="home-banner">
    <swiper class="home-banner__swiper"    
      circular
      autoplay
      indicatorDots
      indicatorActiveColor='rgb(178, 42, 49)'
    >
      <swiper-item class="home-banner__swiper-item">
        <img class="home-banner__swiper-item-img" src="../../../static/images/user.png" alt="">
      </swiper-item>
      <swiper-item class="home-banner__swiper-item">
        <img class="home-banner__swiper-item-img" src="../../../static/images/user.png" alt="">
      </swiper-item>
      <swiper-item class="home-banner__swiper-item">
        <img class="home-banner__swiper-item-img" src="../../../static/images/user.png" alt="">
      </swiper-item>
      <swiper-item class="home-banner__swiper-item">
        <img class="home-banner__swiper-item-img" src="../../../static/images/user.png" alt="">
      </swiper-item>
    </swiper>
  </div>
</template>

<script>

export default {
  data () {
    return{
      picList:[{'url':'../../../static/images/user.png'}]
    }
  }
}
</script>

<style scoped>
.home-banner {
  margin: -30rpx 0 -40rpx;
  height: 410rpx;
  background: #ffffff;
  overflow: hidden;
}

.home-banner__swiper {
  height: 340rpx;
}

.home-banner__swiper-item {
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.home-banner__swiper-img {
  width: 690rpx;
  height: 340rpx;
  border-radius: 8rpx;
  overflow: hidden;
}

</style>