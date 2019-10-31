<template>
  <div class="swipe">
    <van-swipe :autoplay="2000" indicator-color="red">
      <van-swipe-item v-for="(item,index) in banners" :key=index >
          <a :href="item.link">
            <img class="banner-img" :src="item.image" :alt="item.title">
          </a>
      </van-swipe-item>
    </van-swipe>
  </div>
</template>

<script>

export default {
 props:{
   banners:{
     type:Array,
     default(){
       return []
     }
   }
 }

};
</script>

<style scoped>
.banner-img{
    width:100%;
    height: width*.5px;
}
</style>