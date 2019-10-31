<template>
  <div id="cart">
    <nav-bar class="nav-bar">
      <div slot="center">购物车({{cartCount}})</div>
    </nav-bar>
    <scroll class="content">
      <cart-list class="cart-list" :cart-list="cartList"></cart-list>
    </scroll>

    <bottom-bar></bottom-bar>
    <main-tab-bar/>
  </div>
</template>

<script>
import NavBar from "common/navbar/NavBar";
import CartList from "./childComps/CartList";
import BottomBar from "./childComps/BottomBar";
import Scroll from "../../components/common/scroll/Scroll"
import MainTabBar from 'components/content/mainTabbar/MainTabBar'
export default {
  name: "Cart",
  components: {
    NavBar,
    CartList,
    BottomBar,
    Scroll,
    MainTabBar
    
  },
  computed: {
    cartList() {
      return this.$store.getters.cartList;
    },
    cartCount() {
      return this.$store.getters.cartCount;
    }
  }
};
</script>

<style scoped>
#cart {
  /*position: relative;*/
  height: 100vh;
}

.nav-bar {
  background-color: #fff;
  color: #000;
  border-bottom: #ccc 1px solid;
}

.cart-list {
  position: absolute;
  top: 0px;
  bottom: 0px;
  width: 100%;
}
.content {
   position: absolute;
    top: 44px;
    bottom: 49px;
    left: 0;
    right: 0;
}

</style>
