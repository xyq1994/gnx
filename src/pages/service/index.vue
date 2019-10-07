<template>
  <div class="root">
    <div class="top">
      <div class="top-div">
        <img class="img" src="../../../static/photo/info.png" alt="">
        <text>在线客服</text>
      </div>

      <div class="top-div">
        <img class="img" src="../../../static/photo/tel.png" alt="">
        <text>客服热线</text>
      </div>
    </div>
    <div class="middle">
      <text>问题分类</text>
    </div>

    <div class="buttom">
      <div class="buttom-info">
        <img class="info-img" src="../../../static/images/help.png" >
        <text>常见问题</text>
        <img class="info-img1" src="../../../static/photo/white.png" >
      </div>

      <div class="buttom-info">
        <img class="info-img" src="../../../static/images/help.png" >
        <text>配送问题</text>
        <img class="info-img1" src="../../../static/photo/white.png" >
      </div>

      <div class="buttom-info">
        <img class="info-img" src="../../../static/images/help.png" >
        <text>售后问题</text>
        <img class="info-img1" src="../../../static/photo/white.png" >
      </div>

      <div class="buttom-info">
        <img class="info-img" src="../../../static/images/help.png" >
        <text>优惠问题</text>
        <img class="info-img1" src="../../../static/photo/white.png" >
      </div>

      <div class="buttom-info">
        <img class="info-img" src="../../../static/images/help.png" >
        <text>秒杀问题</text>
        <img class="info-img1" src="../../../static/photo/white.png" >
      </div>

      <div class="buttom-info">
        <img class="info-img" src="../../../static/images/help.png" >
        <text>支付问题</text>
        <img class="info-img1" src="../../../static/photo/white.png" >
      </div>

      <div class="buttom-info">
        <img class="info-img" src="../../../static/images/help.png" >
        <text>优币问题</text>
        <img class="info-img1" src="../../../static/photo/white.png" >
      </div>

      <div class="buttom-info">
        <img class="info-img" src="../../../static/images/help.png" >
        <text>会员问题</text>
        <img class="info-img1" src="../../../static/photo/white.png" >
      </div>

      <div class="buttom-info">
        <img class="info-img" src="../../../static/images/help.png" >
        <text>活动问题</text>
        <img class="info-img1" src="../../../static/photo/white.png" >
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.root{
  display: flex;
  flex-direction: column;
  height: 100%;
}
.top{
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  height: 160rpx;
  box-sizing: border-box;
  border-top: 1rpx solid rgba(0,0,0,.15);
  border-bottom: 1rpx solid rgba(0,0,0,.15);
}
.img{
  margin-top: 10rpx;
  height: 90rpx;
  width: 90rpx;
}
.top-div{
  display: flex;
  flex-direction: column;
  align-items: center;
}
/**middle部分 */
.middle{
  display: flex;
  align-items: center;
  height: 90rpx;
}
.middle text{
  margin-left: 35rpx;
}

/**buttom样式 */
.buttom{
  display: flex;
  flex: 1;
  flex-direction: column;
  height: 600rpx;
  box-sizing: border-box;
  border-top: 1rpx solid rgba(0,0,0,.15);
  border-bottom: 1rpx solid rgba(0,0,0,.15);
}
.buttom-info{
  display: flex;
  align-items:center; 
  box-sizing: border-box;
  border-top: 1rpx solid rgba(0,0,0,.15);
  border-bottom: 1rpx solid rgba(0,0,0,.15);
  height: 85rpx;
}
.buttom-info text{
  margin-left: 15rpx;
}
.info-img{
  margin-left: 35rpx;
  height: 40rpx;
  width: 40rpx;
}
.info-img1{
  margin-left: 440rpx;
  height: 60rpx;
  width: 80rpx;
}
</style>