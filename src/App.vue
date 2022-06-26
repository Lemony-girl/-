<template>
  <div class="app">
    <MyHeader></MyHeader>
    <MyGoods></MyGoods>
    <MyFooter></MyFooter>
  </div>
</template>

<script>
import MyHeader from '@/components/MyHeader.vue'
import MyGoods from '@/components/MyGoods.vue'
import MyFooter from '@/components/MyFooter.vue'
export default {
  components: {
    MyHeader,
    MyGoods,
    MyFooter
  }
}
</script>

<style scoped>
.app {
  padding: 50px 0;
}
</style>
