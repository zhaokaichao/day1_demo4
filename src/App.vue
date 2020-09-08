<template>
  <div id="app">
    <h2>父组件</h2>
    <p>子向父发送的数据：{{val}}</p>
    <list :msg='msg' @dataList='parentList'></list>
    <my></my>
  </div>
</template>

<script>
import list from './components/list'
import my from './components/my'
export default {
  name: 'App',
  components: {
    list,my
  },
  data() {
    return {
      msg:'我的父组件传来的',
      val:''
    }
  },
  methods: {
    parentList(data){
      this.val=data
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
