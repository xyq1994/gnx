<template>
  <div class="root">
    <!--订单页面顶部 -->
    <div class="top">
      <img class="top-img" src="../../../static/photo/person-img.png" alt="">
      <div class="top-middle">
        <text>jay-chou  165xxxx1234</text>
        <text>西安市西北大学</text>
      </div>
      <div class="top-btn">
        <span>默认</span>
        <img class="btn-img" src="../../../static/photo/redirect.png" alt="" @click="goAddress">
      </div>
    </div>
    <div class="middle">
      <text>配货清单</text>
    </div>
    <!--订单页面订单详情-->
    <div class="good-list"> 
      <div class="item" v-for="item in priceList" :key="item">
        <img class="item-img" :src=item.img />
        <div class="item-tex">
          <text>GNX套餐-A</text>
          <text>肤色M</text>
          <text>￥{{item.unitPrice}}</text>
        </div>
        <div class="item-counter">
          <div class="item-counter-btn">
            <text @click="subtraction">-</text>
            <text>{{item.number}}</text>
            <text @click="addition">+</text>
          </div>
          <div class="item-counter-price">
            ￥{{item.totlePrice}}
          </div>
        </div>
      </div>
    </div>
    <!--订单页面底部 -->
    <div class="pay">
      <div class="pay-top">
        <text>线下付款</text>
      </div>
      <div class="pay-middle">
        <text>上传付款凭证</text>
        <img class="middle-img" src="../../../static/profile/qr-code.png" alt="">
      </div>
      <div class="pay-buttom">
        <div class="pay-buttom-totle">
          <text>￥{{payMoney}}</text>
        </div>
        <div class="pay-buttom-customer">
          <text>客服</text>
        </div>
        <div class="pay-buttom-buy" @click="toPay(id)">
          <text>立即下单</text>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  data () {
    return{
      priceList:[
        {unitPrice:68, totlePrice:0, number:0, img:'../../static/photo/close.jpg'},
        {unitPrice:84, totlePrice:0, number:0, img:'../../static/photo/close.jpg'},
        {unitPrice:56, totlePrice:0, number:0, img:'../../static/photo/close.jpg'}
      ],
      payMoney:0
    }
  },
  methods: {
    /**页面跳转 */
    toPay () {
      let url = '/pages/order-pay/main?money=' + this.payMoney
      wx.navigateTo({
        url: url,
      });
    },
    goAddress (){
      wx.navigateTo({
        url: '/pages/manage-address/main',
      });
    },
    /**加减法 */
    subtraction(){
      let list = this.priceList;
      for (let index = 0; index < list.length; index++) {
        let element = list[index];
        if (element.number > 0) {
          element.number --
          element.totlePrice = element.totlePrice - element.unitPrice
        }else{
          element.number = 0
        }
      }
      this.payTotle();
    },
    addition(){
      let list = this.priceList;
      for (let index = 0; index < list.length; index++) {
        let element = list[index];
        element.number ++
        element.totlePrice = element.number * element.unitPrice
      }
      this.payTotle();
    },
    /**计算金额 */
    payTotle(){
      let list = this.priceList;
      let money = 0;
      for (let index = 0; index < list.length; index++) {
        let element = list[index];
        money += element.totlePrice;
      }
      this.payMoney = money;
    }
  }
}
</script>

<style>
.root{
  display: flex;
  flex-direction: column;
  height: 100%;
}
/**顶部样式 */
.top{
  display: flex;
  flex-direction: row;
  align-items: center;
  height: 160rpx;
  background: #1ABC9C;
}
.top-img{
  margin: 20rpx 0 20rpx 35rpx;
  height: 80rpx;
  width: 80rpx;
}
.top-middle{
  margin-left: 20rpx;
}
.top-middle text{
  text-align: center;
  margin: 5rpx 0;
  display: block;
}
.top-btn{
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-left: 100rpx;
}
.btn-img{
  height: 80rpx;
  width: 80rpx;
}
/**配货清单 */
.middle{
  height: 85rpx;
  display: flex;
  align-items: center;
  box-sizing: border-box;
  border-top: 1rpx solid rgba(0,0,0,.15);
  border-bottom: 1rpx solid rgba(0,0,0,.15);
}
.middle text{
  margin-left: 35rpx;
}

/** 商品展示*/
.good-list{
  flex: 1;
  display: flex;
  flex-direction: column;
}
.item{
  display: flex;
  flex-direction: row;
  height: 160rpx;
  border-top: 1rpx solid rgba(0,0,0,.15);
  box-sizing: border-box;
}
.item-img{
  height: 140rpx;
  width: 140rpx;
  margin: 10rpx 35rpx;
}
.item-tex{
  display: flex;
  flex-direction: column;
  /* align-items: center; */
  margin: 20rpx 0;
}
.item-tex text{
  padding: 5rpx; 
  font-weight: 500;
  font-size: 24rpx;
  display: block;
}
.item-counter{
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 33.3%;
  margin-left: 140rpx;
}
.item-counter-btn{
  margin: 15rpx 0;
}
.item-counter-btn text{
  padding: 35rpx;
}
.item-counter-price{
  margin: 20rpx 0;
  text-align: center;
}

/**底部部分 */
.pay{
  display: flex;
  flex-direction: column;
  height: 270rpx;
}
.pay-top{
  flex: 1;
  display: flex;
  align-items: center;
  margin-left: 35rpx;
  border-top: 1rpx solid rgba(0,0,0,.15);
  box-sizing: border-box;
}
.pay-middle{
  flex: 1;
  display: flex;
  border-top: 1rpx solid rgba(0,0,0,.15);
  box-sizing: border-box;
  align-items: center;
}
.pay-middle text{
  margin-left: 35rpx;
}
.middle-img{
  margin-left: 420rpx;
  height: 50rpx;
  width: 50rpx;
}
.pay-buttom{
  flex: 1.2;
  border-top: 1rpx solid rgba(0,0,0,.15);
  box-sizing: border-box;
  align-items: center;
  display: flex;
  flex-direction: row;
}
.pay-buttom-totle text{
  margin-left: 35rpx;
}
.pay-buttom-customer text{
  margin-left: 360rpx;
}
.pay-buttom-buy text{

  margin-left: 50rpx;
}
</style>
