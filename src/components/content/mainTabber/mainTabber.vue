<template>
  <div>
    <tab-bar>
      <tab-bar-item path="/home" active-color="#d4237a">
        <img slot="item-icon" src="~assets/img/tabberImg/home.svg" alt="">
        <img slot="item-icon-active" src="~assets/img/tabberImg/home-o.svg" alt="">
        <div slot="item-text">首页</div>
      </tab-bar-item>
      <tab-bar-item path="/category" active-color="#d4237a">
        <img slot="item-icon" src="~assets/img/tabberImg/category.svg" alt="">
        <img slot="item-icon-active" src="~assets/img/tabberImg/category-o.svg" alt="">
        <div slot="item-text">分类</div>
      </tab-bar-item>
      <tab-bar-item path="/cart" active-color="#d4237a">
        <img slot="item-icon" src="~assets/img/tabberImg/cart.svg" alt="">
        <img slot="item-icon-active" src="~assets/img/tabberImg/cart-o.svg" alt="">
        <div slot="item-text">购物车</div>
      </tab-bar-item>
      <tab-bar-item path="/profile" active-color="#d4237a">
        <img slot="item-icon" src="~assets/img/tabberImg/profile.svg" alt="">
        <img slot="item-icon-active" src="~assets/img/tabberImg/profile-o.svg" alt="">
        <div slot="item-text">我的</div>
      </tab-bar-item>
    </tab-bar>
  </div>
</template>

<script>
  import TabBar from 'components/common/tabber/TabBar'
  import TabBarItem from 'components/common/tabber/TabBarItem'

  export default {
    name: "mianTabber",
    components: {
      TabBar,
      TabBarItem
    }
  }
</script>

<style scoped>

</style>
