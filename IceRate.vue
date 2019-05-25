<template>
  <div class="ice-rate">
    <span
      v-for="i in max"
      @click="readonly?:currentCount=i"
      :style="{color:i<=currentCount?selectColor:defaultColor}"
      class="iconfont icon-Starlarge ice-rate-item"></span>
  </div>
</template>

<script>
  export default {
    name: "IceRate",
    props: {
      defaultColor: {
        type: String,
        default: 'gray'
      },
      selectColor: {
        type: String,
        default: '#FFD566'
      },
      max: {
        type: Number,
        default: 5
      },
      value: {
        type: Number,
        default: 0
      },
      readonly:{
        type:Boolean,
        default:false
      }
    },
    model:{
      prop:'vlaue',
      event:'input'
    },
    data(){
      return{
        currentCount:this.value
      }
    },
    watch:{
      currentCount(){
        this.$emit('input',this.currentCount);
      },
      value(){
        this.currentCount=this.value;
      },
    }
  }
</script>

<style scoped>
  @import "./iconfont/iconfont.css";
  .ice-rate-item{
    font-size: 20px;
  }
</style>
