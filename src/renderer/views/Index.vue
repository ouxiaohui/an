<template>
   <div>
       hello
   </div>
</template>

<script>
export default {
  name: "Index",
  data() {
    return {
      singers: []
    };
  },
  filters: {
    avatar: function(value) {
      if (!value) return "";
      return value.replace(/{size}/, "200");
    }
  },
  created() {
    // this.fetchHotSingerList();
  },
  methods: {
    fetchHotSingerList() {
      const url = "http://m.kugou.com/singer/list/88&json=true";
      this.$http.get(url).then(res => {
        this.singers=res.data.singers.list.info

      }, error => {

      })
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .singer-list{
    display: flex;
    flex-wrap: wrap;
  }
  .singer-list li{
    width: 200px;
    margin-right: 2%;
    margin-bottom: 10px;

    box-shadow: 0px 3px 1px -2px rgba(0, 0, 0, 0.2), 0px 2px 2px 0px rgba(0, 0, 0, 0.14), 0px 1px 5px 0px rgba(0, 0, 0, 0.12);
    color: #232323;
    background-color: #fff;
  }
  .singer-list img{
    width: 200px;
    height: 200px;
  }
  .singer-list .singer-name{
    /* display: block; */
    padding: 8px;
  }

</style>
