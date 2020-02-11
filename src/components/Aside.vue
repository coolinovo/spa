<template>
  <div style="width: 15rem;" class="aside-wrapper">
    <div class="user-avatar">
      <a href="#" :title="username">
        <img :src="avatar" :alt="username">
      </a>
    </div>
    <div class="user-count">
      <div><span>Articles</span>1</div>
      <div><span>Tags</span>1</div>
      <div><span>Categories</span>1</div>
    </div>
    <div class="aside-tools">
      <router-link to="/">
        <a href="#" :class="['tools-item', this.$route.name === 'Main'?'active':'']">
          <i class="el-icon-s-home" :style="{ 'color':this.$route.name === 'Main'?'#fff':'#9ca2a8'}"></i>
          <div class="tools-item-content">回到首页</div>
        </a>
      </router-link>
      <router-link to="/about">
        <a href="#" :class="['tools-item', this.$route.name === 'About'?'active':'']">
          <i class="el-icon-info" :style="{ 'color':this.$route.name === 'About'?'#fff':'#9ca2a8'}"></i>
          <div class="tools-item-content">关于博客</div>
        </a>
      </router-link>
      <router-link to='/list'>
        <a href="#"  :class="['tools-item', this.$route.name === 'List'?'active':'']">
          <i class="el-icon-user" :style="{ 'color':this.$route.name === 'List'?'#fff':'#9ca2a8'}"></i>
          <div class="tools-item-content">我的朋友</div>
        </a>
      </router-link>
    </div>
    <aside class="aside-sidebar">
      <div class="widget-wrap">
        <div class="search">
          <form action="" id="search_form"><label><input placeholder="Search" type="search"></label></form>
        </div>
      </div>
      <div class="widget-wrap">
        <h3 class="widget-title">Social</h3>
        <div class="social">

        </div>
      </div>
      <div class="widget-wrap">
        <h3 class="widget-title">Archive</h3>
        <div class="widget-time">
          <ul class="archive-list">
            <li class="archive-list-item">
              <a href="#" class="item-href">February 2020</a>
            </li>
          </ul>
        </div>
      </div>
    </aside>
    <div class="copyright">
      &copy; 2020 Yeh Lin
      Powered by
      <a href="#">Vue</a>&
      <a href="#">element</a>
    </div>
  </div>
</template>

<script>
  import router from '../router/index'
  export default {
    name: 'sidebar',
    data() {
      return {
        avatar: 'https://cdn.jsdelivr.net/gh/nexmoe/nexmoe.github.io@latest/images/avatar.png',
        username: 'coolin'
      }
    },
    router,
    mounted() {
      console.log(this.$route)
    },
    methods: {
    }
  }
</script>

<style lang='less' scoped>
  .aside-wrapper {
    /*border: 1px solid #ccc;*/
    height: 100vh;
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    z-index: 5000;
    width: calc(100% - 56px);
    max-width: 280px;
    margin: 0;
    overflow-x: hidden;
    overflow-y: auto;
    white-space: nowrap;
    will-change: transform;
    margin-left: -240px;

    .user-avatar {
      margin: 3rem;
      z-index: 4;
      position: relative;
      font-size: 0;
      width: calc(100% - 6.5rem);
      overflow: hidden;
      border-radius: 100%;
      box-shadow: 0 0.3rem 2rem rgba(161, 177, 204, .6);

      a {
        padding-bottom: 100%;
        display: block;
        height: 0;
        background-color: transparent;
        text-decoration: none;
        cursor: pointer;
        color: -webkit-link;

        img {
          width: 100%;
          -webkit-border-radius: 5.33rem;
          transition: transform 1.5s ease-out;
          border-style: none;
        }
      }
    }

    .user-count {
      padding: 0 30px;
      margin-bottom: 30px;
      display: flex;

      div {
        -webkit-box-flex: 1;
        flex: 1;
        text-align: center;
        color: #a3a8ae;

        span {
          color: #363636;
          display: block;
          margin-bottom: 3px;
        }
      }
    }

    .aside-tools {
      padding: 8px 20px;
      margin: 0;
      list-style: none;
      background-color: transparent;

      .tools-item {
        padding: 0 36px;
        color: #9ca2a8;
        transition: all .35s;
        border-radius: 10px;
        margin-bottom: 10px;
        text-align: center;
        text-decoration: none;
        display: flex;
        min-height: 48px;
        -webkit-box-align: center;
        align-items: center;
        position: relative;
        overflow: hidden;
        user-select: none;

        &:after {
          height: 48px;
          visibility: hidden;
          content: ' ';
        }

        i {
          line-height: 1.15;
          white-space: nowrap;
          list-style: none;
          user-select: none;
          cursor: pointer;
          text-align: center;
          box-sizing: border-box;
          -webkit-tap-highlight-color: transparent;
          width: 24px;
          min-width: 24px;
          height: 24px;
          font-size: 22px;
          color: #9ca2a8;
        }

        .tools-item-content {
          margin-left: 0;
          transition: all .35s;
          padding-top: 14px;
          padding-bottom: 14px;
          font-size: 1.07rem;
          font-weight: 400;
          line-height: 20px;
          -webkit-box-flex: 1;
          flex-grow: 1;
        }
      }
    }

    .aside-sidebar {

      .widget-wrap {
        box-shadow: 0 0 1rem rgba(161, 177, 204, .4);
        background-color: #fff;
        margin: 20px;
        border-radius: 10px;
        overflow: hidden;
        white-space: normal;

        .search {

          #search_form {

            input {
              border: none !important;
              background-color: transparent;
              padding: 20px;
              box-sizing: border-box;
              outline: 0;
            }
          }
        }

        .widget-title {
          font-size: 1.2em;
          font-weight: 400;
          padding: 12px 10px 10px;
          border-bottom: 1px solid #eee;
          margin: 0;
        }

        .social {
          padding: 5px;
        }

        ul {
          list-style-type: none;
          padding: 0;
          margin: 0;

          li:last-child {
            border-bottom: none;
            overflow: hidden;
            text-overflow: ellipsis;
            white-space: nowrap;
            position: relative;

            a {
              padding: 14px 10px;
              display: block;
              color: #606266;
              position: relative;
              overflow: hidden;
              cursor: pointer;
              user-select: none;
            }
          }
        }
      }

      &:first-child {
        margin-top: 0;

        [type = search] {
          -webkit-appearance: textfield;
          outline-offset: -2px;
        }
      }
    }

    .copyright {
      padding: 0 30px;
      text-align: center;
      color: #777;
      white-space: normal;
      margin-bottom: 20px;

      a {
        color: rgba(255,78,106,.8);
      }
    }
  }
  .active {
    color: #fff !important;
    opacity: .9;
    background: #ff4e6a;
    box-shadow: 0 2px 12px #ff4e6a;
    padding: 0 36px;
    transition: all .35s;
    border-radius: 10px;
    margin-bottom: 10px;
    text-align: center;
  }
</style>