<template>
  <div class="home-policy">
    <div class="home-policy__item">
      <img class="home-policy__item-img" src="" alt="">
      <text class="home-policy__item-txt"></text>
    </div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style scoped>
.home-policy {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 36rpx 30rpx 28rpx;
  background: #ffffff;
}

.home-policy__item {
  display: flex;
  flex-direction: row;
  align-items: center;
}
.home-policy__item-img {
    margin-right: 14rpx;
    width: 28rpx;
    height: 28rpx;
}

.home-policy__item-txt {
  color: #666666;
  font-size: 24rpx;
  line-height: 24rpx;
}
</style>