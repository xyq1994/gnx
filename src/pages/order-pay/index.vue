<template>
  <div class="root">
    <img class="order-img" src="../../../static/photo/order-success.png" alt="">
    <div class="order-text">
      <text>订单提交成功</text>
      <text>请在客户指引下完成线下付款流程</text>
      <text>待支付金额￥{{payMoney}}</text>
    </div>
    <div class="order-btn">
      <button @click="goOrder">查看订单</button>
      <button @click="goIndex">回到首页</button>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      payMoney:'',
    }
  },
  methods:{
    getQuery() {
      let pages = getCurrentPages() //获取加载的页面
      let currentPage = pages[pages.length-1] //获取当前页面的对象
      let url = currentPage.route //当前页面url
      let options = currentPage.options //如果要获取url中所带的参数可以查看options
      this.payMoney = options.money
    },
    goOrder(){
      wx.navigateTo({
        url: '/pages/child-order/main',
      });
    },
    goIndex(){
      wx.switchTab({
        url: '/pages/index/main',
      });
    }
  },
  mounted() {
    this.getQuery()
  },
}
</script>

<style scoped>
.root{
  display: flex;
  flex-direction: column;
  align-items: center;
  background: #ffffff;
}
.order-img{
  height: 240rpx;
  width: 300rpx;
}
.order-text{
  display: flex;
  flex-direction: column;
  align-items: center;
}
.order-text text{
  margin: 15rpx;
}
.order-btn{
  margin: 15rpx 0;
}
.order-btn button{
  margin: 15rpx;
  display: inline;
}
</style>