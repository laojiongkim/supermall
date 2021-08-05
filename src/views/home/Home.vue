<template>
    <div id="home">
        <nav-bar class="home-nav"><div slot="center">购物街</div></nav-bar>
        <home-swiper :banners="banners" />
        <recommend-view :recommends="recommends" />
        <feature-view></feature-view>
        <ul>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
          <li>列表</li>
        </ul>
    </div>
    
</template>
<script>
import NavBar from "../../components/common/navbar/NavBar";
import HomeSwiper from './childComps/HomeSwiper'
import { getHomeMultidata } from "../../network/home";
import RecommendView from './childComps/RecommendView';
import FeatureView from './childComps/FeatureView'
// import FeatureView from './childComps/FeatureView.vue';

export default {
  name: "Home",
  components: {
    NavBar,
    HomeSwiper,
    RecommendView,
    FeatureView
    // FeatureView
  },
  data() {
    return {
      banners: [],
      recommends: []
    }
  },
  created() {
    getHomeMultidata().then((res) => {
      this.banners = res.data.banner.list;
      this.recommends = res.data.recommend.list;
    });
  },
};
</script>

<style scoped>
#home{
  padding-top: 44px; 
}

.home-nav {
  background-color: var(--color-tint);
  color: #fff;
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  z-index: 9;
}
</style>