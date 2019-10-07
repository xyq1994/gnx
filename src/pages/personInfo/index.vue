<template>
  <div class="root">
    <div class="top">
      <img src="../../../static/photo/head.jpg" alt="">
      <text>点击修改头像</text>
    </div>
    <div class="blank"></div>
    <div class="middle">
      <div class="Id">
        <text class="inline">用户ID</text>
        <input class="inline" type="text" v-model="Id" placeholder="123456">
      </div>
      <div class="Id">
        <span class="inline">昵称</span>
        <input class="inline" type="text" v-model="Id" placeholder="tom">
      </div>
      <div class="Id">
        <span class="inline">性别</span>
        <input class="inline" type="text" v-model="Id" placeholder="男">
      </div>
      <div class="Id">
        <span class="inline">生日</span>
        <input class="inline" type="text" v-model="Id" placeholder="123456">
      </div>
      <div class="Id">
        <span class="inline">城市</span>
        <input class="inline" type="text" v-model="Id" placeholder="123456">
      </div>
      <div class="Id">
        <span class="inline">职业</span>
        <input class="inline" type="text" v-model="Id" placeholder="123456">
      </div>
      <div class="Id">
        <span class="inline">个性签名</span>
        <input class="inline" type="text" v-model="Id" placeholder="123456">
      </div>
    </div>
    <div class="buttom">

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
  flex-direction: column;
  align-items: center;
  height: 260rpx;
  box-sizing: border-box;
  border-top: 1rpx solid rgba(0,0,0,.15);
  border-bottom: 1rpx solid rgba(0,0,0,.15);
}
.top img{
  height: 130rpx;
  width: 130rpx;
  border-radius: 50%;
  margin: 20rpx 0;
}
.top text{
  margin: 10rpx 0;
}
.blank{
  height: 30rpx;
}
/**middle部分 */
.middle{
  height:280rpx;
}
.Id{
  display: flex;
  flex-direction: row;
  align-items: center;
  height: 80rpx;
  box-sizing: border-box;
  border-top: 1rpx solid rgba(0,0,0,.15);
  border-bottom: 1rpx solid rgba(0,0,0,.15);
}
.inline{
  margin: 0 35rpx;
}
</style>