<template>
  <div class="app">
    <MyHeader title="购物车" :background="'black'" color="gold"></MyHeader>
    <MyGoods
      v-for="item in list"
      :key="item.goods_id"
      :item="item"
      :list="list"
    ></MyGoods>
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
  },
  data () {
    return {
      list: []
    }
  },
  created () {
    this.getList()
  },
  methods: {
    async getList () {
      const res = await this.$axios({ url: '/api/cart' })
      console.log(res)
      this.list = res.data.list
      console.log(this.list)
    }
  }
}
</script>

<style scoped>
.app {
  padding: 50px 0;
}
</style>
