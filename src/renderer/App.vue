<template>
  <div id="app">
     <side></side>
    <router-view></router-view>
  </div>
</template>

<script>
  import Side from './components/Side'
  export default {
    name: 'an',
      components:{
        Side
      }
  }
</script>

<style>
  /* CSS */
  * {
    box-sizing: border-box;
  }
  body{
    color: #fff;
    background-color: #232323;
  }

  body,ul {
    margin: 0;
  }

  h1 {
    margin-top: 0;
    margin-bottom: 0;
  }

  li {
    list-style: none;
  }
</style>
