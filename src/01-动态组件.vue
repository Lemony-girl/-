<template>
  <div>
    <h1>(*^▽^*)</h1>
    <button @click="componentName = 'MyAccount'">点击变Account</button>
    <button @click="componentName = 'MyInfo'">点击变Info</button>
    <keep-alive>
      <component :is="componentName"></component>
    </keep-alive>
  </div>
</template>

<script>
import MyAccount from '@/components/MyAccount.vue'
import MyInfo from '@/components/MyInfo.vue'
export default {
  components: {
    MyAccount,
    MyInfo
  },
  data () {
    return {
      componentName: 'MyAccount'
    }
  }
}
</script>

<style>
</style>
