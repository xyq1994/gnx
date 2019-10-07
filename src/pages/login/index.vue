<template>
  <div class="root">
    <div class="top">
      <img src="../../../static/photo/login.png" alt="">
    </div>
    <div class="middle">
      <div class="Id">
        <text class="inline">telphone</text>
        <input class="inline1" type="text" v-model="telphone" placeholder="输入手机号码">
      </div>
      <div class="Id">
        <span class="inline">password</span>
        <input class="inline1" type="password" v-model="password" placeholder="短信验证码">
      </div>
    </div>
    <div class="submit">
      <button class="btn" @click="goIndex">确认</button>
    </div>
  </div>
</template>
 
<script>
export default {
  data(){
    return{
      userInfo:{uTelphone:'15512345678',uPassword:'123456'},
      telphone:'',
      password:'',
    }
  },
  methods:{
    login(){
      let that = this;
      let letPhone = this.telphone;
      let letPsw = this.password;
      let params = {};
      parmas.telphone = letPhone;
      parmas.letPsw = letPsw;

      var reqTask = wx.request({
        url: 'http://121.41.47.68:8080/renren-admin/login',
        data: {},
        header: {'content-type':'application/json'},
        method: 'GET',
        dataType: 'json',
        responseType: 'text',
        success: (result)=>{
          
        },
        fail: ()=>{},
      });
    },
    checkPhone(PhoneNumber){
      var rePhone = /^1[0-9]{10}/;
      if (rePhone.test(PhoneNumber)){
        return true;
      }else{
        return false;
      }
    },
    goIndex(){
      let that = this;
      let letPhone = this.telphone;
      let letPsw = this.password;
      if (this.checkPhone(letPhone)) {
        if (this.userInfo.uPassword == letPsw) {
          wx.switchTab({
            url: '/pages/index/main',
          });
        } else {
          wx.showModal({
            title: '温馨提示',
            content: '密码有误，请重新输入',
            showCancel:false,
            confirmText: '确定',
            confirmColor: '#3CC51F',
            success: (result) => {
              if(result.confirm){
                that.password = ''
              }
            },
          });
        }
      } else {
        wx.showModal({
          title: '温馨提示:',
          content: '输入手机号码错误，请重新输入',
          showCancel: false,
          confirmText: '确定',
          confirmColor: '#3CC51F',
          success: (result) => {
            if(result.confirm){
              that.telphone = ''
              that.password = '' 
            }
          },
        });
      }
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
  flex-direction: column;
  align-items: center;
  box-sizing: border-box;
}
.top img{
  height: 220rpx;
  width: 260rpx;
  margin: 80rpx 0;
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
  width: 80%;
  box-sizing: border-box;
  border-bottom: 1rpx solid rgba(0,0,0,.15);
  margin-left: 60rpx;
  margin-top: 5rpx;
}
.inline{
  margin: 0 35rpx;
}
/**buttom底部样式 */
.buttom{
  display: flex;
  flex-direction: row;
  align-items: center;
}
.buttom-img{
  height: 60rpx;
  width: 60rpx;
  margin-left: 65rpx;
}
.submit{
  display: flex;
  align-items: center;
  margin: 30rpx;
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