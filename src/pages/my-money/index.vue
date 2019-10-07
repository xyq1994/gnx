<template>
  <div class="root">
    <div class="money">
      <img src="../../../static/photo/money.png" alt="">
      <div class="tex">
        <text>2019年8月分红</text>
        <text>2000</text>
      </div>
    </div>
    <div class="middle">
      <div>
        <text>团队业绩</text>
        <text>￥300</text>
      </div>
      <div>
        <text>平推记录</text>
        <text>￥26</text>
      </div>
      <div>
        <text>其他</text>
        <text>￥10</text>
      </div>
    </div>
    <div class="buttom">
      <div class="bom">
        <text class="bom-text">2019年7月</text>
        <text class="number">2000</text>
        <div class="div">
          <text>团队 12,000</text>
          <text>平推 50,000</text>
          <text>其他 31,000</text>
        </div>
      </div>
      <div class="bom">
        <text class="bom-text">2019年7月</text>
        <text class="number">2000</text>
        <div class="div">
          <text>团队 12,000</text>
          <text>平推 50,000</text>
          <text>其他 31,000</text>
        </div>
      </div>
      <div class="bom">
        <text class="bom-text">2019年7月</text>
        <text class="number">2000</text>
        <div class="div">
          <text>团队 12,000</text>
          <text>平推 50,000</text>
          <text>其他 31,000</text>
        </div>
      </div>
      <div class="bom">
        <text class="bom-text">2019年7月</text>
        <text class="number">2000</text>
        <div class="div">
          <text>团队 12,000</text>
          <text>平推 50,000</text>
          <text>其他 31,000</text>
        </div>
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
}
/**顶部样式 */
.money{
  display: flex;
  flex-direction: column;
  align-items: center;
  background: #1ABC9C;
  height: 300rpx;
}
.money img{
  margin: 25rpx 0;
  height: 120rpx;
  width: 140rpx;
}
.tex text{
  display: block;
  margin: 5rpx 0;
  text-align: center;
}
/**中间部分 */
.middle{
  display: flex;
  height: 110rpx;
  justify-content: space-around;
  align-items: center;
  box-sizing: border-box;
  border-top: 1rpx solid rgba(0,0,0,.15);
  border-bottom: 1rpx solid rgba(0,0,0,.15);
}
.middle text{
  display: block;
  text-align: center;
}
/**底部样式 */
.buttom{
  display: flex;
  flex-direction: column;
}
.bom{
  display: flex;
  flex-direction: column;
  height: 220rpx;
  border-bottom: 1rpx solid rgba(0,0,0,.15);
}
.bom div{
  margin: 10rpx 0;
}
.bom-text{
  margin: 15rpx 35rpx;
  font-weight: bold;
}
.number{
  margin: 15rpx 35rpx;
}
.bom .div text{
  margin: 15rpx 0 15rpx 35rpx;
}
</style>