<template>
  <div class="root">
    <div class="top">
      <img class="image" src="../../../static/photo/head.jpg" alt="">
      <div class="info">
        <text>rose jeack</text>
        <text>VIP1</text>
      </div>
      <img class="redirect" @click="goPerson" src="../../../static/photo/image.png" alt="">
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
    goPerson(){
      wx.navigateTo({
        url: '/pages/person/main',
      });
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
.top{
  display: flex;
  height: 280rpx;
  align-items: center;
  flex-direction: row;
  background: #464C5B;
}
.image{
  height: 150rpx;
  width: 150rpx;
  margin: 0 30rpx 0 55rpx;
  border-radius: 50%;
}
.info text{
  color: white;
  display: block;
  margin: 25rpx 0;
  text-align: center;
}
.redirect{
  margin-left: 260rpx;
  height: 80rpx;
  width: 80rpx;
}
</style>