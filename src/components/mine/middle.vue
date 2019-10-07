<template>
  <div class="middle">
    <div class="middle-one" @click="goMoney">
      <text class="middle_text">累计分红</text>
      <text class="middle_text">2300</text>
    </div>
    <div class="middle-two">
      <text class="middle_text">本月分红</text>
      <text class="middle_text">100</text>
    </div>
  </div>
</template>
<script>
export default {
  data (){
    return{

    }
  },
  methods:{
    goMoney(){
      wx.navigateTo({
        url: '/pages/my-money/main',
      });
    }
  }
}
</script>
<style scoped>
.middle{
  display: flex;
  align-items: center;
  justify-content: space-around;
  height: 100rpx;
  width: 100%;
  background-color: white;
  margin: 10rpx 0;
  border: 0 solid rgba(0,0,0,.15);
  border-bottom-width: 1rpx;
}
.middle-one{
  display: flex;
  flex-direction: column;
  align-items: center
}
.middle-two{
  display: flex;
  flex-direction: column;
  align-items: center
}
.middle_text{
  color: #333;
  font-size: 24rpx;
  font-weight: normal;
  line-height: 24rpx;
  margin-top: 16rpx;
}
</style>