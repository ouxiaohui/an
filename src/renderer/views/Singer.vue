<template>
   <div></div>
</template>

<script>
export default {
  name: "Singer",
  data() {
    return {
      singerId: null
    };
  },
  filters: {
    avatar: function(value) {
      if (!value) return "";
      return value.replace(/{size}/, "200");
    }
  },
  created() {
    this.fetchSingerInfo();
  },
  methods: {
    fetchSingerInfo() {
      var _this = this;
      var url = `http://m.kugou.com/app/i/getSongInfo.php?cmd=playInfo&hash=F9429A116529E3547A47E79D732EC2C9&from=mkugou`;
      fetch(url)
        .then(function(response) {
          return response.json();
        })
        .then(function(res) {

        });
    }
  }
};
</script>


<style scoped>

</style>
