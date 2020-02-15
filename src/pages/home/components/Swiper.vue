<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: require('../../../assets/image/swiper1.jpg')
      }, {
        id: '0002',
        imgUrl: require('../../../assets/image/swiper2.png')
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
      background: red !important
  .wrapper
    width: 100%
    height: 31.25vw
    background: #eee
    .swiper-img
      width: 100%
      height: 31.25vw
</style>
