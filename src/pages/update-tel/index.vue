<template>
  <div class="root">
   <div class="top">
     <div :class=" mark ? 'active' : '' ">
       <text>1.验证原号码</text>
     </div>
     <div :class=" mark ? '': 'active' ">
       <text>2.绑定新手机</text>
     </div>
   </div>
   <div class="black"></div>

   <div class="middle" v-if="show">
     <div>
      <input type="text" v-model="telPhone" placeholder="请输入手机号码">
     </div>
     <div>  
      <input type="text" v-model="code" placeholder="请输入验证码">
     </div>
   </div>
  <div class="middle" v-else>
     <div>
      <input type="text" v-model="newTelPhone" placeholder="请输入新手机号码">
     </div>
     <div>  
      <input type="text" v-model="newCode" placeholder="请输入验证码">
     </div>
   </div>

    <div class="submit" v-if="show">
      <button class="btn" @click="nextStep">下一步</button>
    </div>
    <div class="submit" v-else>
      <button class="btn">确定</button>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      mark:true,
      show:true
    }
  },
  methods: {
    nextStep () {
      this.mark = ! this.mark;
      this.show = ! this.show;
    }
  }
}
</script>

<style scoped>
.root{
  display: flex;
  flex-direction: column;
  height: 100%;
  background: #f9f9f9;
}
.top{
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-around;
  box-sizing: border-box;
  border-top: 1rpx solid rgba(0,0,0,.15);
  border-bottom: 1rpx solid rgba(0,0,0,.15);
  height: 100rpx;
}
.black{
  height: 25rpx;
}

/**middle部分 */
.middle{
  display: flex;
  flex-direction: column;
  background: #ffffff;
}
.middle div{
  display: flex;
  align-items: center;
  height: 80rpx;
  box-sizing: border-box;
  border-top: 1rpx solid rgba(0,0,0,.15);
}
.middle div input{
  margin-left: 35rpx;
}
.active{
  background: red;
}
.submit{
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 50rpx;
  height: 120rpx;
  width: 80%;
}
.btn{
  margin-left: 50rpx;
  border-radius: 50rpx;
  height: 90rpx;
  width: 90%;
  background: #1ABC9C;
}
</style>