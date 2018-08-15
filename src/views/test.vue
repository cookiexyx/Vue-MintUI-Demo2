<template>
    <div id="test">
        <a href="">test</a>
        <ul>
          <li v-for="(item,index) in listData" :key="index">{{item.femalename}}</li>
        </ul>
    </div>
</template>
<script>
export default {
  name: 'test',
  data () {
    return {
      listData: []
    }
  },
  created () {
    this.getList()
  },
  methods: {
    getList () {
      this.$http.get('https://www.apiopen.top/femaleNameApi', {
        params: {
          page: 1
        }
      }).then(res => {
        this.listData = res.data.data
      }).catch(err => {
        console.log(err)
      })
    }
  }
}
</script>
<style lang="scss">
#test{
  ul{
    li{
      width: 100%;
      height: 24px;
      line-height: 24px;
      font-size: 16px;
      border-bottom: 1px #f3f3f3 solid;
      text-align: left;
      padding: 0 20px;
    }
  }
}
</style>
