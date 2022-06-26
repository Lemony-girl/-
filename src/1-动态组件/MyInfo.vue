<template>
  <div>
    <label>
      <span>人生格言:</span>
      <input type="text" placeholder="请输入账号" />
    </label>

    <br />

    <label>
      <span>自我介绍:</span>
      <textarea cols="20" rows="5"></textarea>
    </label>
  </div>
</template>

<script>
export default {
  created () {
    console.log('MyInfo被创建')
  },
  activated () {
    console.log('MyInfo被激活')
  },
  deactivated () {
    console.log('MyInfo失活')
  },
  destroyed () {
    console.log('MyInfo销毁')
  }
}
</script>

<style></style>
