<template>
  <div class="list">
      <h2>子组件</h2>
      <p>{{msg}}</p>
      <input type="text" v-model="val">
      <button @click='childPass'>发送数据</button>
  </div>
</template>

<script>
export default {
    name:'list',
    data(){
        return {
            val:''
        }
    },
    props:{
        msg:{
            type:String,
            default:'默认值'
        }
    },
    methods: {
        childPass(){
            this.$emit('dataList',this.val)
        }
    },
}
</script>

<style>

</style>