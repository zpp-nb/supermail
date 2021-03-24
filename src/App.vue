<template>
  <div id="app">
    <router-view/>
    <MainTabBar/>
  </div>
</template>
<script>''
import MainTabBar from 'components/content/mainTabber/mainTabber'

export default {
  name: 'app',
  components: {
    MainTabBar
  }
}
</script>
<style>
  @import "./assets/css/base.css";
</style>
