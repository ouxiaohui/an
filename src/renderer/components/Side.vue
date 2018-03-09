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
          },
            {
                id:2,
                text:'FM'
            },
            {
                id:3,
                text:'MV'
            },
            {
                id:4,
                text:'Local'
            },
            {
                id:5,
                text:'Download'
            }
        ]
      }
    }
  }
</script>

<style scoped>
    #side ul{
        padding: 4px 0;
    }
   #side li{
    height: 40px;
    padding: 0 16px;
}
</style>
