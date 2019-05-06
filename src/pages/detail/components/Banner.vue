<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1904/6e/6edffb73a665bc70a3.img.jpg_600x330_68d52ff1.jpg" />
      <div class="banner-info">
        <div class="banner-title">
          上海海洋水族馆(AAAA景区)
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe612;</span>
          39
        </div>
      </div>
    </div>
    <CommonGallery
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGallaryClose"
    ></CommonGallery>
  </div>
</template>

<script>
import CommonGallery from 'common/gallary/Gallary'
export default {
  name: 'Banner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1412/9f/fbff2a5302c0ce906ef9b64159730f89.water.jpg_r_800x800_de6503c8.jpg',
        'http://img1.qunarzz.com/sight/p0/201301/08/4905cefd7787e37e93835fbb.jpg_r_800x800_5b2bc2ee.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallery
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
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, .8))
      .banner-title
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
