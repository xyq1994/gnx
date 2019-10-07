<template>
  <div class="root">
    <div class="Id">
      <span class="inline">旧密码</span>
      <input class="inline" type="password" v-model="Id" placeholder="请输入就密码">
    </div>
    <div class="Id">
      <span class="inline">新密码</span>
      <input class="inline" type="password" v-model="Id" placeholder="请输入新密码(6-20位)">
    </div>
    <div class="Id">
      <span class="inline">确认密码</span>
      <input class="inline" type="password" v-model="Id" placeholder="请再次输入确认新密码">
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