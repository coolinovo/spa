<template>
  <div class="main-content">
    <div class="primary">
      List
    </div>
  </div>
</template>

<script>
export default {
  name: 'list'
}
</script>

<style lang='less' scoped>
  .main-content {
    position: relative;
    width: 960px;
    /*height: 100%;*/

    .primary {
      box-shadow: 0 0 1rem rgba(161, 177, 204, .5);
      background-color: #fff;
      float: left;
      width: 100%;
      padding: 20px;
      position: absolute;
      min-height: 100vh;
    }
  }
</style>