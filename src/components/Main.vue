<template>
  <div class="main-content">
    <div class="primary">
      <section>
        <div class="post">
          <div class="post-cover">
            <img :src="bgc" alt="123" sizes="920px">
            <h1>Hello World</h1>
          </div>
          <div class="post-meta">
            <a><i class="font icon-calendar-fill"></i>2020年02月10日</a>
            <a><i class="font icon-areachart"></i>73 字</a>
            <a><i class="font icon-time-circle-fill"></i>大概 1 分钟</a>
          </div>
          <article>

          </article>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: 'mainContent',
  data() {
    return {
      bgc: 'https://cdn.jsdelivr.net/gh/nexmoe/nexmoe.github.io@latest/images/cover/5c3aec85a4343.jpg'
    }
  }
}
</script>

<style lang='less' scoped>
.main-content {
  position: relative;
  width: 960px;
  /*height: 100%;*/

  .primary {
    box-shadow: 0 0 1rem rgba(161,177,204,.5);
    background-color: #fff;
    float: left;
    width: 100%;
    padding: 20px;
    position: absolute;
    min-height: 100vh;

    section {
      position: relative;

      .post:last-child {
        margin-bottom: 20px;
        width: 100%;

        .post-cover {
          padding-bottom: 66.6666666666%;
          width: 100%;
          position: relative;
          overflow: hidden;
          border-radius: 10px;
          margin-bottom: 10px;
          min-height: 75px;
          background-color: #eee;
          cursor: pointer;
          user-select: none;

          img {
            width: 100%;
            display: block;
            transition: filter .4s ease-in, -webkit-filter .4s ease-in;
            position: absolute;
            left: 0;
            top: 0;
            opacity: 1;
            filter: blur(0);
          }

          h1 {
            line-height: 1.15;
            font-family: Roboto,Noto,Helvetica,Arial,sans-serif;
            cursor: pointer;
            user-select: none;
            -webkit-tap-highlight-color: transparent;
            position: absolute;
            bottom: 0;
            padding: 20px;
            color: #fff;
            font-size: 2.2em;
            width: 100%;
            box-sizing: border-box;
            text-transform: none;
            z-index: 1;
            margin: 0;
            font-weight: 400;
          }
        }

        .post-meta {
          line-height: 1.15;
          font-family: Roboto,Noto,Helvetica,Arial,sans-serif;
          color: rgba(0,0,0,.87);
          font-size: 15px;
          box-sizing: border-box;
          -webkit-tap-highlight-color: transparent;
          margin-bottom: -10px;

          & a:nth-child(7n+1) {
            line-height: 1.15;
            font-family: Roboto,Noto,Helvetica,Arial,sans-serif;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
            text-decoration: none;
            border-radius: 10px;
            padding: 6px 10px;
            color: #fff;
            font-size: 14px;
            display: inline-block;
            margin-bottom: 5px;
            margin-right: 3px;
            background-color: #ff4e6a;
          }

          & a:nth-child(7n+2) {
            line-height: 1.15;
            font-family: Roboto,Noto,Helvetica,Arial,sans-serif;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
            text-decoration: none;
            border-radius: 10px;
            padding: 6px 10px;
            color: #fff;
            font-size: 14px;
            display: inline-block;
            margin-bottom: 5px;
            margin-right: 3px;
            background-color: #ffaa73;
          }

          & a:nth-child(7n+3) {
            line-height: 1.15;
            font-family: Roboto,Noto,Helvetica,Arial,sans-serif;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
            text-decoration: none;
            border-radius: 10px;
            padding: 6px 10px;
            color: #fff;
            font-size: 14px;
            display: inline-block;
            margin-bottom: 5px;
            margin-right: 3px;
            background-color: #fed466;
          }
        }

        & article {
          line-height: 1.15;
          font-size: 15px;
          box-sizing: border-box;
          -webkit-tap-highlight-color: transparent;
          color: #444;
          font-family: microsoft yahei;
          padding: 10px 0;
        }
      }
    }
  }
}
</style>