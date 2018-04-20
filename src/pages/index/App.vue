<template>
  <div id="app">
    <db-header></db-header>
    <top-banner></top-banner>
    <router-view/>
  </div>
</template>

<script>
  import DBHeader from '../../components/DBHeader'
  import TopBanner from './components/TopBanner'

  export default {
    name: 'App',
    components: {
      'db-header': DBHeader,
      TopBanner
    }
  }
</script>

<style>
  * {
    margin: 0;
    padding: 0;
  }

  #app {
   /* font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;*/
    text-align: center;
    color: #2c3e50;
    width: inherit;
  }

  html{
    font-size: 13px;
  }

</style>
