<template>
  <div id="side">
      <ul>
          <li v-for="item in nav" :key="item.nav">{{item.text}}</li>
      </ul>
  </div>
</template>

<script>
  export default {
    name: "Side",
    data(){
      return{
        nav:[
          {
            id:0,
            text:'Discover'
          }
        ]
      }
    }
  }
</script>

<style scoped>
#side {

}
</style>
