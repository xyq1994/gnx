<template>
  <div class="user">
    <person></person>
    <middle></middle>
    <menuPage></menuPage>
    <div class="user-middle"></div>
    <div class="user-buttom">
      <div class="buttom-info" @click="goAddress">
        <img class="info-img" src="../../../static/images/help.png" >
        <text>信息变更</text>
        <img class="info-img1" src="../../../static/photo/white.png" >
      </div>
      <div class="buttom-info" @click="goService">
        <img class="info-img" src="../../../static/images/help.png" >
        <text>服务中心</text>
        <img class="info-img1" src="../../../static/photo/white.png" >
      </div>
      <div class="buttom-info">
        <img class="info-img" src="../../../static/images/help.png" >
        <text>业绩查询</text>
        <img class="info-img1" src="../../../static/photo/white.png" >
      </div>
      <div class="buttom-info">
        <img class="info-img" src="../../../static/images/help.png" >
        <text>合伙人升级</text>
        <img class="info-img2" src="../../../static/photo/white.png" >
      </div>
    </div> 
  </div>
</template>

<script>

import person from '../../components/mine/person'
import middle from '../../components/mine/middle'
import menuPage from '../../components/mine/menuPage'

export default {
  components: {
    person,
    middle,
    menuPage
  },

  data () {
    return {
     
    }
  },

  methods:{
    goAddress(){
      wx.navigateTo({
        url: '/pages/manage-address/main',
      });
    },
    goService(){
      wx.navigateTo({
        url: '/pages/service/main',
      });
    }
  }
}
</script>

<style>
.user {
  position: relative;
}
.user-middle{
  height: 80rpx;
  background: #f9f9f9;
}
.user-buttom{
  display: flex;
  flex-direction: column;
}
.buttom-info{
  flex: 1;
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
.info-img2{
  margin-left: 408rpx;
  height: 60rpx;
  width: 80rpx;
}
</style>
