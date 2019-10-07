<template>
  <div class="root">
    <div class="top">
      <img class="image" src="../../../static/photo/head.jpg" alt="">
      <div class="info">
        <text>个人主页</text>
      </div>
      <text class="enter">进入</text>
      <img class="redirect" src="../../../static/photo/white.png" alt="">
    </div>
    <div class="middle"></div>
    <div class="buttom">
      <div class="person" @click="goInfo">
        <text>个人信息</text>
        <img class="info-img" src="../../../static/photo/white.png" alt="">
      </div>
      <div class="person" @click="goUpdatePsw">
        <text>修改密码</text>
        <img class="info-img" src="../../../static/photo/white.png" alt="">
      </div>
      <div class="person" @click="goUpdateTel">
        <text>修改手机</text>
        <img class="info-img" src="../../../static/photo/white.png" alt="">
      </div>
      <div class="person" @click="goTeam">
        <text>我的会员</text>
        <img class="info-img" src="../../../static/photo/white.png" alt="">
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return{

    }
  },
  methods:{
    goInfo(){
      wx.navigateTo({
        url: '/pages/personInfo/main',
      });
    },
    goUpdatePsw(){
      wx.navigateTo({
        url: '/pages/update-psw/main',
      });
    },
    goUpdateTel(){
      wx.navigateTo({
        url: '/pages/update-tel/main',
      });
    },
    goTeam(){
      wx.navigateTo({
        url: '/pages/my-team/main',
      });
    },
  }
}
</script>
<style scoped>
.root{
  display: flex;
  flex-direction: column;
  height: 100%;
}
/**个人主页 */
.top{
  display: flex;
  height: 280rpx;
  align-items: center;
  flex-direction: row;
  background: #FFFFFF;
  box-sizing: border-box;
  border-top: 1rpx solid rgba(0,0,0,.15);
  border-bottom: 1rpx solid rgba(0,0,0,.15);
}
.image{
  height: 150rpx;
  width: 150rpx;
  margin: 0 30rpx 0 55rpx;
  border-radius: 50%;
}
.info text{
  display: block;
  margin: 25rpx 0;
  text-align: center;
}
.enter{
  margin-left: 200rpx;
}
.redirect{
  height: 70rpx;
  width: 100rpx;
}
/**中间部分 */
.middle{
  height: 50rpx;
}
.info-img{
  height: 70rpx;
  width: 100rpx;
}
.person{
  display: flex;
  flex-direction: row;
  align-items: center;
  height: 80rpx;
  background: #FFFFFF;
  box-sizing: border-box;
  border-top: 1rpx solid rgba(0,0,0,.15);
  border-bottom: 1rpx solid rgba(0,0,0,.15);
}
.person text{
  margin: 0 55rpx;
}
.person img{
  margin-left: 390rpx;
}
</style>