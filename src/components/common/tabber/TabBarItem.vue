<template>
  <div class="tab-bar-item" @click="itemClick" :style="activeFob">
    <div v-if="isActive">
      <slot  name="item-icon-active"></slot>
    </div>
    <div v-else>
      <slot  name="item-icon"></slot>
    </div>
    <div :style="activeStyle">
      <slot  name="item-text"></slot>
    </div>
  </div>
</template>

<script>
  export default {
    name: "TabBarItem",
    props:{
      path:'',
      //动态活跃颜色
      activeColor:{
        type:String,
        default:'red'
      }
    },
    data() {
      return {
      }
    },
    computed:{
      //当活跃的路由和当前路由一致时，就返回true
      isActive(){
        return this.$route.path.indexOf(this.path) !==-1
      },
      //当前活跃的颜色改变
      activeStyle(){
        return this.isActive ? {color:this.activeColor} : {}
      },
      //当前活跃的被禁用（防止二次点击）
      activeFob(){
        return this.isActive ? {pointerEvents: 'none'} : {}
      }
    },
    methods:{
      itemClick(){
        this.$router.replace(this.path)
      }
    }
  }
</script>

<style scoped>
  .tab-bar-item {
    /*水平布局*/
    flex: 1;
    /*文字居中*/
    text-align: center;
    /*流行高度*/
    height: 49px;
    font-size: 14px;
  }

  .tab-bar-item img {
    width: 24px;
    height: 24px;
    margin-top: 3px;
    /*取消图片下默认的3px*/
    /*改成2px*/
    vertical-align: middle;
    margin-bottom: 2px;
  }
</style>
