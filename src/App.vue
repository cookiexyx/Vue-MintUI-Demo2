<template>
  <div id="app">
    <mt-header fixed title="标题过长会隐藏后面的内容啊哈哈哈哈">
      <router-link to="/" slot="left">
          <mt-button icon="back">返回</mt-button>
      </router-link>
      <mt-button icon="more" slot="right"></mt-button>
    </mt-header>
      <router-view/>
    <mt-tabbar fixed class="footer">
      <mt-tab-item id="out">
        外卖
      </mt-tab-item>
      <mt-tab-item id="order">
        订单
      </mt-tab-item>
      <mt-tab-item id="my">
        我的
      </mt-tab-item>
    </mt-tabbar>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  .footer{
    height: 40px;
    line-height: 40px;
  }
}
</style>
