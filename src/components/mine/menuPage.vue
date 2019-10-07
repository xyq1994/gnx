<template>
  <div class="user-menu">
    <div class="user-menu__item" v-for="(item,index) in menuList" :key="index" @click="jump(item.routeurl)">
      <img class="user-menu__item-img" :src=item.url />
      <text class="user-menu__item-txt">{{item.title}}</text>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return{
      menuList:[
        {'title':'我的订单','url':'../../static/images/feedback.png','routeurl':'/pages/child-order/main'},
        {'title':'待付款','url':'../../static/images/feedback.png','routeurl':'/pages/child-order/main'},
        {'title':'待收货','url':'../../static/images/feedback.png','routeurl':'/pages/child-order/main'},
        {'title':'已完成','url':'../../static/images/feedback.png','routeurl':'/pages/child-order/main'},
        {'title':'团队订单','url':'../../static/images/feedback.png','routeurl':'/pages/group-order/main'},
        {'title':'待发货','url':'../../static/images/feedback.png','routeurl':'/pages/group-order/main'},
        {'title':'我的分红','url':'../../static/images/feedback.png','routeurl':'/pages/my-money/main'},
        {'title':'我的团队','url':'../../static/images/feedback.png','routeurl':'/pages/my-team/main'}
      ]
    }
  },
  methods: {
    jump (url) {
      wx.navigateTo({
        url: url
      });
    }
  }
}
</script>
<style scoped>
.user-menu {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  background: #fff;
}
.user-menu__item {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  box-sizing: border-box;
  /* border: 1rpx solid rgba(0,0,0,.15); */
  border-bottom: 1rpx solid rgba(0,0,0,.15);
  /* border-bottom-width: 1rpx;
  border-right-width: 1rpx; */
  width: 25%;
  height: 120rpx;
}
.user-menu__item-img{
  width: 52rpx;
  height: 52rpx;
}
.user-menu__item-txt{
  margin-top: 16rpx;
  color: #333;
  font-size: 24rpx;
  line-height: 24rpx;
}
</style>