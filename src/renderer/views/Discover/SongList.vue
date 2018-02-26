<template>
    
</template>

<script>
    export default {
        name: "SongList",
        created(){
          this.getBestSongList();
        },methods:{
            getBestSongList(){
               // this.$http.get('http://localhost:3000/top/playlist/highquality?limit=30').then((res)=>{
               //     console.log(res)
               // }).catch((error)=>{
               //
               // })
            }
        }
    }
</script>

<style scoped>

</style>