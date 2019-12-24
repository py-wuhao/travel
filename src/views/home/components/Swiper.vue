<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="showSwiper">
      <swiper-slide v-for="item of list" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
    name: "HomeSwiper",
    data () {
        return {
            list: [
                {'id':1,
                'imgUrl':'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201912/4400f4a848b1f5920c64b801deba4692.jpg_750x200_c9a739ba.jpg'
                },
                {
                    'id':2,
                     'imgUrl':'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201912/d6df0db510d7b9aaa3d9ce4cffafeca1.jpg_750x200_abb38f14.jpg'

                }
            ],
            swiperOption: {
                pagination: '.swiper-pagination',
                loop: true
            }
        }
    },
    computed: {
        showSwiper () {
        return this.list.length
        }
    }
};
</script>

<style lang='stylus' scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 26.57%
    background: #eee
    .swiper-img
      width: 100%
</style>
