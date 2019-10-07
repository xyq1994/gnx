<template>
  <div class="root">
    <div class="item">
      <div class="order-num">
        <text class="num">订单编号:124567</text>
        <!-- <slot name='right-tex'></slot> -->
        <text class="tex">等待付款</text>
      </div>
      <div class="order-list" v-for="item in orderList" :key="item">
        <img class="order-img" :src=item.url alt="">
        <div class="good-cont">
          <text>棕色休闲mini短袖</text>
          <text>肤色/M</text>
          <text>￥99</text>
        </div>
        <text class="counter">x1</text>
      </div>
      <div class="order-buttom">
        <!-- <slot name="left"></slot>
        <slot name="middle"></slot>
        <slot name="right"></slot> -->
        <text>应付金额:￥180</text>
        <span>取消订单</span>
        <span>上传付款凭证</span>
      </div>
      <div class="end"></div> 
    </div>

        <div class="item">
      <div class="order-num">
        <text class="num">订单编号:124567</text>
        <!-- <slot name='right-tex'></slot> -->
        <text class="tex">等待付款</text>
      </div>
      <div class="order-list" v-for="item in orderList" :key="item">
        <img class="order-img" :src=item.url alt="">
        <div class="good-cont">
          <text>棕色休闲mini短袖</text>
          <text>肤色/M</text>
          <text>￥99</text>
        </div>
        <text class="counter">x1</text>
      </div>
      <div class="order-buttom">
        <!-- <slot name="left"></slot>
        <slot name="middle"></slot>
        <slot name="right"></slot> -->
        <text>应付金额:￥180</text>
        <span>取消订单</span>
        <span>上传付款凭证</span>
      </div>
      <div class="end"></div> 
    </div>

        <div class="item">
      <div class="order-num">
        <text class="num">订单编号:124567</text>
        <!-- <slot name='right-tex'></slot> -->
        <text class="tex">等待付款</text>
      </div>
      <div class="order-list" v-for="item in orderList" :key="item">
        <img class="order-img" :src=item.url alt="">
        <div class="good-cont">
          <text>棕色休闲mini短袖</text>
          <text>肤色/M</text>
          <text>￥99</text>
        </div>
        <text class="counter">x1</text>
      </div>
      <div class="order-buttom">
        <!-- <slot name="left"></slot>
        <slot name="middle"></slot>
        <slot name="right"></slot> -->
        <text>应付金额:￥180</text>
        <span>取消订单</span>
        <span>上传付款凭证</span>
      </div>
      <div class="end"></div> 
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      orderList:[
        {'url':'../../static/photo/close.jpg'},
        {'url':'../../static/photo/close.jpg'},
        {'url':'../../static/photo/close.jpg'}
      ]
    }
  }
}
</script>

<style scoped>
.root{
  display: flex;
  flex-direction: column;
  height: 100%;
}
.item{
  display: flex;
  flex-direction: column;
}
.order-num{
  display: flex;
  align-items: center;
  height: 80rpx;
  box-sizing: border-box;
  border-top: 1rpx solid rgba(0,0,0,.15);
  border-bottom: 1rpx solid rgba(0,0,0,.15);
}
.num{
  margin-left: 35rpx;
}
.tex{
  margin-left: 300rpx;
  color: #F15E5B
}
.num-list{
  height: 20rpx;
  background: #F9F9F9;
}
/**商品订单展示 */
.order-list{
  display: flex;
  flex-direction: row;
  margin: 15rpx 0;
  border-bottom: 1rpx solid rgba(0,0,0,.15);
}
.order-img{
  margin: 15rpx 35rpx;
  height: 140rpx;
  width: 140rpx;
}
.good-cont text{
  display: block;
  margin: 10rpx;
}
.counter{
  margin-top: 10rpx;
  margin-left: 190rpx;
}
/**底部样式 */
.order-buttom{
  display: flex;
  flex-direction: row;
  align-items: center;
  height: 70rpx;
  box-sizing: border-box;
  border-bottom: 1rpx solid rgba(0,0,0,.15);
}
.order-buttom text{
  margin-left: 35rpx;
  margin-right: 100rpx;
}
.order-buttom span{
  box-sizing: border-box;
  border: 1rpx solid rgba(0,0,0,.15);
  border-radius: 5rpx;
  margin: 10rpx;
}
/**结尾样式 */
.end{
  height:20rpx;
  background: #F9F9F9;
}
</style>