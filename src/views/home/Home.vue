<template>
  <div id="home">
    <nav-bar class="home-nav">
      <div slot="center">购物车</div>
    </nav-bar>
    <home-swiper :banners="banners"></home-swiper>
  </div>
</template>

<script>
  import NavBar from "components/common/navbar/NavBar"
  import {getHomeMultidata} from "network/home"
  import HomeSwiper from "./ChildComps/HomeSwiper"
  export default {
    name: 'Home',
    components: {
      NavBar,
      HomeSwiper
    },
    data() {
      return {
        banners: [],
        recommends: [],
      }
    },
    created() {
      getHomeMultidata().then(res => {
          this.banners = res.data.banner.list;
          this.recommends = res.data.recommend.list;
      })
    },
    computed: {},
    methods: {},
    mounted() {

    },
    destroyed() {

    },
    activated() {

    },
    deactivated() {

    }
  }
</script>

<style scoped>
  #home {
    /* padding-top: 44px; */
    height: 100vh;
    position: relative;
  }

  .home-nav {
    background-color: var(--color-tint);
    color: #fff;
    /*
      position: fixed;
      left: 0;
      right: 0;
      top: 0;
      z-index: 9; */
  }

  .tab-control {
    position: relative;

    z-index: 9;
  }

  .content {
    overflow: hidden;

    position: absolute;
    top: 44px;
    bottom: 49px;
    left: 0;
    right: 0;
  }
</style>
