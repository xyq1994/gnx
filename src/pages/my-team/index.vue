<template>
  <div class="root">
    <div class="top">
      <img class="image" src="../../../static/photo/head.jpg" alt="">
      <span>tom</span>
      <img class="member" src="../../../static/photo/member.png" alt="">
    </div>
    <div class="black"></div>
    <div class="middle">
      <div class="team">
        <text>团队成员</text>
      </div>
      <div class="info" v-for="(item,index) in teamUsers" :key="index">
        <img :src=item.uImg>
        <div class="info-tex">
          <text>{{item.uName}}</text>
          <text>加入时间:{{item.uDate}}</text>
          <text>累计提成:{{item.uScore}}</text>
        </div>
        <div class="appraise">
          <text>评价</text>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      teamUsers:[
        {uName:'张三',uDate:'2019-5-7',uScore:'2000',uImg:'../../static/photo/head.jpg'},
        {uName:'李四',uDate:'2019-5-7',uScore:'2000',uImg:'../../static/photo/head.jpg'},
        {uName:'王五',uDate:'2019-5-7',uScore:'2000',uImg:'../../static/photo/head.jpg'},
        {uName:'赵六',uDate:'2019-5-7',uScore:'2000',uImg:'../../static/photo/head.jpg'}
      ]
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
  height: 430rpx;
  box-sizing: border-box;
  border-top: 1rpx solid rgba(0,0,0,.15);
  border-bottom: 1rpx solid rgba(0,0,0,.15);
}
.image{
  margin: 35rpx 0;
  height: 140rpx;
  width: 140rpx;
  border-radius: 50%;
}
.member{
  margin: 20rpx 0;
  height: 120rpx;
  width: 80%;
}
.black{
  height: 60rpx;
  background: #f9f9f9;
}
/**middle部分 */
.middle{
  background: #ffffff;
}
.team{
  display: flex;
  align-items: center;
  height: 95rpx;
  box-sizing: border-box;
  border-top: 1rpx solid rgba(0,0,0,.15);
}
.team text{
  margin-left: 35rpx;
}
/**团队成员部分 */
.info{
  display: flex;
  flex-direction: row;
  align-items: center;
  box-sizing: border-box;
  border-top: 1rpx solid rgba(0,0,0,.15);
  border-bottom: 1rpx solid rgba(0,0,0,.15);
}
.info img{
  margin: 10rpx 35rpx;
  height: 140rpx;
  width: 140rpx;
}
.info-tex text{
  margin: 5rpx 10rpx;
  display: block;
}
.appraise text{
  margin-left: 100rpx;
}
</style>