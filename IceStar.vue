<template>
  <div class="ice-star">
    <span
      v-for="i in max"
      @click="currentCount=i"
      :style="{color:i<=currentCount?selectColor:defaultColor}"
      class="ice-star-item iconfont icon-Starlarge"></span>
  </div>
</template>

<script>
  export default {
    name: "IceStar",
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
    }
  }
</script>

<style scoped>
  @import "./iconfont/iconfont.css";

</style>
