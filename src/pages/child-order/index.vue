<template>
  <div class="root">
    <bar/>
    <goodsList>
    </goodsList>
  </div>
</template>

<script>
import bar from '../../components/child-order-component/bar'
import goodsList from '../../components/child-order-component/goods-list'
export default {
  components:{
    bar,
    goodsList
  }
}
</script>

<style scoped>

</style>