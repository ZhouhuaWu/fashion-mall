<template>
  <div id="detail">

  </div>
</template>

<script>


export default {
  name: 'Detail',
  data() {
    return {

    }
  },

  created(){


  },
  methods:{

  },

  components:{

  }
 }
</script>

<style scoped>
  #detail {
    height: 100vh;
    position: relative;
    z-index: 9;
    background-color: #fff;
  }

  .content {
    position: absolute;
    top: 44px;
    bottom: 60px;
  }
  .detail-nav{
    position: relative;
    z-index: 9;
    background: #fff;
  }

  .back-top {
    position: fixed;
    right: 10px;
    bottom: 65px;
  }
</style>
