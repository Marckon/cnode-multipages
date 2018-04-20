<template>
  <div class="top-banner">
    <div class="search-area">
      <div class="nav-logo">
        <a href="/">豆瓣电影</a>
      </div>
      <input type="text" placeholder="搜索电影、电视剧、综艺、影人" class="sear-text" size="22" maxlength="60">
      <input type="submit" class="sear-btn" value="">
    </div>
    <div class="navs">
      <template v-for="nav in navs">
        <router-link :to="nav.path">{{nav.name}}</router-link>
      </template>
    </div>
  </div>
</template>

<script>
  export default {
    name: "TopBanner",
    data() {
      return {
        navs: [
          {
            name: '影讯&购票',
            path: '/'
          },
          {
            name: '选电影',
            path: '/'
          },
          {
            name: '电视剧',
            path: '/movie'
          },
          {
            name: '排行榜',
            path: '/'
          },
          {
            name: '分类',
            path: '/'
          },
          {
            name: '影评',
            path: '/'
          },
          {
            name: '2017年度榜单',
            path: '/'
          },
          {
            name: '2017观影报告',
            path: '/'
          },
        ]
      }
    }
  }
</script>

<style lang="less">
  .top-banner {
    height: 115px;
    background-color: #f0f3f5;

    .search-area {
      height: 75px;
      border-bottom: solid #e3ebec 1px;
      width: 1040px;
      margin: 0 auto;
      display: flex;
      align-items: center;

      .nav-logo {
        a {
          font-size: 2.5em;
          color:#238ccd;
          font-weight: bold;
          text-decoration: none;
        }
      }

      .sear-text{
        margin-left: 20px;
        height:30px;
        width:40%;
        outline: none;
        box-shadow: #ccc -1px 1px 1px;
        border-top-left-radius: 5px;
        border-bottom-left-radius: 5px;
        border: none;
      }

      .sear-btn{
        height:30px;
        width:40px;
        background: url("//img3.doubanio.com/dae/accounts/resources/19507ad/movie/assets/nav_mv_bg.png?s=1") no-repeat -39px -40px;
        border: none;
        border-bottom-right-radius: 5px;
        border-top-right-radius:5px ;
      }
    }
  }
</style>
