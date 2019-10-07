<template>
  <div class="root">
    <div class="top">
      <swiper class="top-swiper"  circular autoplay indicatorDots indicatorActiveColor='#FFFFFF'>
        <swiper-item class="swiper-item">
          <img  class="image" src="../../../static/photo/duanxiu.jpg" alt="">
        </swiper-item>
        <swiper-item class="swiper-item">
          <img  class="image" src="../../../static/photo/duanxiu.jpg" alt="">
        </swiper-item>
        <swiper-item class="swiper-item">
          <img  class="image" src="../../../static/photo/duanxiu.jpg" alt="">
        </swiper-item>
      </swiper>
    </div>
    <div class="middle">
      <img class="voice" src="../../../static/photo/voice.png" alt="">
      <text>GNX代理模式火热上线</text>
    </div>
    <div class="black"></div>
    <div class="buttom">
      <div class="buttom-start">
        <text>精选推荐</text>
      </div>
      <div class="buttom-img">
        <img class="pro-img" src="../../../static/photo/duanxiu.jpg" alt="">
      </div>
    </div>
    <div class="tex">
      <div class="pro1">
        <text>GNX套餐1</text>
        <text>洗护好物</text>
      </div>
      <div class="pro2">
        <text>69元起</text>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  data () {
    return {
      
    }
  },

  components: {

  },

  methods: {
  
  },

  created () {
   
  }
}
</script>

<style scoped>
.root{
  display: flex;
  flex-direction: column;
  height: 100%;
}
.image{
  width: 100%;
}
/**middle文字滚动部分 */
.middle{
  display: flex;
  flex-direction: row;
  align-items: center;
  height: 105rpx;
}
.middle img{
  height: 80rpx;
  width: 80rpx;
}
.black{
  height: 30rpx;
  background: #f9f9f9;
}
/**精选推荐 */
.buttom-start{
  display: flex;
  align-items: center;
  height: 90rpx;
}
.buttom-start text{
  margin-left: 35rpx;
}
.pro-img{
  height: 220rpx;
  width:100%;
}

/**产品说明 */
.tex{
  display: flex;
  flex-direction: row;
  align-items: center;
  height: 120rpx;
}
.pro1{
  display: flex;
  flex-direction: column;
  align-items: center;
}
.pro1 text{
  display: block;
  margin-left: 35rpx;
}
.pro2{
  display: flex;
  align-items: center;
}
.pro2 text{
  margin-left: 280rpx;
}
</style>
