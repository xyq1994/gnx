<template>
  <div class="root">
    <div class="address">
      <radio-group class="radio-group" @click="radioChange()">
        <radio class="radio" v-for="item in items" :key="item" :checked=item.checked>
          <div class="radio-cont">
            <text class="name">{{item.name}}  {{item.tel}}</text>   
            <text>{{item.address}}</text>
            <!-- <img class="radio-img" :src=item.img >  -->
          </div>
        </radio>
      </radio-group> 
    </div>
    <div class="add-address">
      <div class="add">
        添加新收货人
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return{
      items: [
        { name: 'tom', tel:'159xxxx1234', address: '西安市软件科技园A区', img:'../../static/photo/update-address.png', checked:'true'},
        { name: 'tom', tel:'159xxxx1234', address: '西安市软件科技园A区', img:'../../static/photo/update-address.png'},
        { name: 'tom', tel:'159xxxx1234', address: '西安市软件科技园A区', img:'../../static/photo/update-address.png'},
        { name: 'tom', tel:'159xxxx1234', address: '西安市软件科技园A区', img:'../../static/photo/update-address.png'},
        { name: 'tom', tel:'159xxxx1234', address: '西安市软件科技园A区', img:'../../static/photo/update-address.png'}
      ]
    }
  },
  methods:{
    radioChange(){
      console.log("click me");
      
    },
  }
}
</script>

<style scoped>
.root{
  display: flex;
  flex-direction: column;
  height: 100%;
}
.address{
  display: flex;
  flex-direction: column;
  height: 160rxp;
}
.radio-group{
  display: flex;
  flex-direction: column;
}
.radio-cont{
  height: 120rpx;
}
.radio-cont text{
  margin: 20rpx 30rpx;
}
.name{
  display: block;
}
.radio{
  height: 160rpx;
  margin: 10rpx 35rpx;
  box-sizing: border-box;
  border-top: 1rpx solid rgba(0,0,0,.15);
  border-bottom: 1rpx solid rgba(0,0,0,.15);
}
.radio-img{
  height: 120rpx;
  width: 120rpx;
}
.add{
  color: #1ABC9C;
  position:fixed;
  bottom:20 rpx;
  left:260rpx;
}
</style>