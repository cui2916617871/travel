<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1412/94/f92c61fbbd2285a2d444e928782f0dcb.water.jpg_350x240_e498cf0c.jpg" />
      <div class="banner-info">
        <div class="banner-tittle">
          侧his侧二十多的
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe692;</span>
          39
        </div>
      </div>
    </div>
      <common-gallary
        :imgs="imgs"
        v-show="showGallary"
        @close="handleGallaryClose"
      ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
// import FadeAnimation from 'common/fade/FadeAnimation'
export default {
  name: 'DetailBanner',
  data(){
      return {
          showGallary:false,
          imgs:["http://img1.qunarzz.com/sight/p0/1507/36/ce3d2d6c9ab44d67ae68d940b8781829.water.jpg_600x330_f68eb231.jpg",
            "http://img1.qunarzz.com/sight/p0/1412/94/f92c61fbbd2285a2d444e928782f0dcb.water.jpg_350x240_e498cf0c.jpg"
          ]
      }
  },
  components:{
      CommonGallary
  },
  methods:{
      handleBannerClick(){
          this.showGallary = true
      },
      handleGallaryClose(){
          this.showGallary = false
      }
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-tittle
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        line-height: .32rem
        margin-top: .14rem
        padding: 0 .4rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
