<template>
  <div class="cart-empty">
    <img class="cart-empty__img" src="../../../static/images/empty.png" />
    <text class="cart-empty__txt">未登录</text>
  </div>
</template>
<script>

export default {
  
}
</script>
<style scoped>
.cart-empty {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 20rpx;
  padding: 140rpx 0 150rpx;
  background: #ffffff;
}

.cart-empty__img {
  width: 260rpx;
  height: 260rpx;
}

.cart-empty__txt {
  margin-top: -8rpx;
  color: #999999;
  font-size: 28rpx;
  line-height: 28rpx;
}
.cart__login {
  margin-top: -80px;
  padding: 0 30px;
}
</style>