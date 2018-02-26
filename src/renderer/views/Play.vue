<template>
    <div class="play">
      {{song.singerName}}
      <audio :src="song.url" controls="controls">
      </audio>
    </div>
</template>

<script>
    export default {
        name: "Play",
      data(){
          return{
           song:''
          }
      },
      created() {
        this.fetchSongInfo();
      },
      methods:{
          fetchSongInfo(){
            const url='http://m.kugou.com/app/i/getSongInfo.php?cmd=playInfo&hash=F9429A116529E3547A47E79D732EC2C9&from=mkugou'
            this.$http.get(url).then(res => {
             this.song=res.data;
            }, error => {

            })
          }
      }
    }
</script>

<style scoped>

</style>
