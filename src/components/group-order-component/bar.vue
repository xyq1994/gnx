<template>
  <div class="root">
    <div class="top-bar">
      <div>待付款</div>
      <div>待收货</div>
      <div>已完成</div>
      <div>已取消</div>
    </div>
    <div class="end"></div>
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
.top-bar{
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
  height: 90rpx;
  border-top: 1rpx solid rgba(0,0,0,.15);
  border-bottom: 1rpx solid rgba(0,0,0,.15);
}
.end{
  height: 20rpx;
  background: #f9f9f9;
}
</style>