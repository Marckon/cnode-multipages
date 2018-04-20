<template>
    <div class="db-header">
      <div class="tabs">
        <template v-for="tab in headerTabs">
          <router-link :to="tab.path">{{tab.name}}</router-link>
        </template>
      </div>
      <div class="extends">
        <router-link to="/">下载豆瓣客户端</router-link>
        <a href="/login.html">登录</a>
        <a href="/register.html">注册</a>
      </div>
    </div>
</template>

<script>
    export default {
        name: "db_header",
      data() {
        return {
          headerTabs: [
            {
              name: '豆瓣',
              path: '/'
            },
            {
              name: '读书',
              path: '/'
            },
            {
              name: '电影',
              path: '/movie'
            },
            {
              name: '音乐',
              path: '/'
            },
            {
              name: '同城',
              path: '/'
            },
            {
              name: '小组',
              path: '/'
            },
            {
              name: '阅读',
              path: '/'
            },
            {
              name: 'FM',
              path: '/'
            },
            {
              name: '时间',
              path: '/'
            },
            {
              name: '市集',
              path: '/'
            },
            {
              name: '更多',
              path: '/'
            }
          ]
        }
      }
    }
</script>

<style>
.db-header{
  height:30px;
  display: flex;
  background-color: #545652;
  justify-content: space-between;
  align-items: center;
}
.db-header .tabs,.extends{
  line-height: 100%;
}
  .db-header a{
    color: #d5d5d5;
    text-decoration: none;
    margin: 0 1em;
  }
</style>
