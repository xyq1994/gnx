<template>
  <div class="home-pin">
    
    <div class="home-pin__banner">
      <!-- <div class="home-pin__banner-item">
        <img class="home-pin__banner-item-img" src="" />
      </div> -->
    </div>

    <div class="home-pin__wrap">
      <swiper class='home-pin__swiper'
        autoplay
        indicatorDots
        indicatorActiveColor='rgb(178, 42, 49)'>

        <swiper-item class="home-pin__swiper-item">

          <div class="home-pin__item">
            <img class="home-pin__item-img" src="../../../static/images/demo.jpg" />
            <div class="home-pin__item-info">
              <text class="home-pin__item-price">拼团价</text>
               <text class="home-pin__item-origin">￥16</text>
            </div>
            <div class="home-pin__item-num">
              <text class="home-pin__item-num-txt">5人团</text>
            </div>
          </div>

          <div class="home-pin__item">
            <img class="home-pin__item-img" src="../../../static/images/demo.jpg" />
            <div class="home-pin__item-info">
              <text class="home-pin__item-price">拼团价</text>
               <text class="home-pin__item-origin">￥16</text>
            </div>
            <div class="home-pin__item-num">
              <text class="home-pin__item-num-txt">5人团</text>
            </div>
          </div>
          
          <div class="home-pin__item">
            <img class="home-pin__item-img" src="../../../static/images/demo.jpg" />
            <div class="home-pin__item-info">
              <text class="home-pin__item-price">拼团价</text>
               <text class="home-pin__item-origin">￥16</text>
            </div>
            <div class="home-pin__item-num">
              <text class="home-pin__item-num-txt">5人团</text>
            </div>
          </div>
        </swiper-item>

        <swiper-item class="home-pin__swiper-item">
          <div class="home-pin__item">
            <img class="home-pin__item-img" src="../../../static/images/demo.jpg" />
            <div class="home-pin__item-info">
              <text class="home-pin__item-price">拼团价</text>
               <text class="home-pin__item-origin">￥16</text>
            </div>
            <div class="home-pin__item-num">
              <text class="home-pin__item-num-txt">5人团</text>
            </div>
          </div>
        </swiper-item>

      </swiper>
    </div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style scoped>
.home-pin {
  padding: 0 30rpx;
  background: #ffffff;
}

.home-pin__banner {
  display: flex;
  flex-direction: column;
}

.home-pin__banner-item {
  display: flex;
  flex-direction: row;
}

.home-pin__banner-img {
  width: 100%;
  height: 170rpx;
}

.home-pin__wrap {
  margin: -100rpx 0 -20rpx;
  height: 450rpx;
  overflow: hidden;
}

.home-pin__swiper {
  height: 330rpx;
}

.home-pin__swiper-item {
  display: flex;
  flex-direction: row
}

.home-pin__item {
  position: relative;
  display: flex;
  flex-direction: column;
  padding: 10rpx;
  overflow: hidden;
}

.home-pin__item-img {
    width: 216rpx;
    height: 216rpx;
    border-radius: 4rpx;
}

.home-pin__item-info {

  
    display: flex;
    flex-direction: row;
    justify-content: center;
    margin-top: 20rpx;
}

.home-pin__item-price {
    color: #ab2b2b;
    font-size: 24rpx;
    line-height: 24rpx;
}

.home-pin__item-origin {
    padding-left: 8rpx;
    color: #999999;
    font-size: 24rpx;
    font-weight: 200;
    line-height: 24rpx;
    text-decoration: line-through;
    text-decoration-color: #999999;
}

.home-pin__item-num {
  position: absolute;
  top: 10rpx;
  left: 10rpx;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  width: 132rpx;
  height: 48rpx;
  background: #ff7d05;
  border-radius: 8rpx 0;
  transform: scale(0.5) translate(-33rpx, -12rpx);
}

.home-pin__item-txt {
  color: #ffffff;
  font-size: 36rpx;
}

</style>