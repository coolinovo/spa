<template>
  <div id="app">
    <div class="app-bgc"></div>
    <el-row>
      <el-col :span="4">
        <Aside/>
      </el-col>
      <el-col :span="20">
        <router-view></router-view>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import router from './router'
import Aside from './components/Aside'
import Main from './components/Main'
import About from './components/About'
import List from './components/List'

export default {
  name: 'app',
  components: {
    Aside,
    Main,
    About,
    List
  },
  router
}
</script>

<style lang="less" scoped>
  .app-bgc {
    background-image: url(https://cdn.jsdelivr.net/gh/nexmoe/nexmoe.github.io@latest/images/cover/5c3aec85a4343.jpg);
    opacity: .2;
    background-size: cover;
    filter: blur(30px);
    width: 100%;
    height: 100vh;
    position: fixed;
    top: 0;
    left: 0;
    z-index: -1;
  }
</style>
