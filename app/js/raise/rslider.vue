<template lang="html">
  <Panel title="金融头条" :class="$style.panel">
    <section :class="$style.content">
      <swiper :options="options">
        <swiper-slide><p>百万白条券免费送，速来领取！！！！！！！</p><em>></em> </swiper-slide>
        <swiper-slide><p>签到领流量，1元500M！</p><em>></em> </swiper-slide>
      </swiper>
    </section>
  </Panel>
</template>

<script>
import { swiper, swiperSlide } from 'vue-awesome-swiper'
import Panel from '../core/panel.vue'
export default {
  components:{
    Panel,
    swiper,
    swiperSlide,
  },
  data(){
    return {
      options: {
        autoplay: true,
        loop: true,
        direction: "vertical",
      },
    }
  }
}
</script>
<style lang="scss">
  .swiper-container-vertical{
    height: 72px;
    .swiper-slide{
      font-family: PingFangSC-Medium;
      font-size: 28px;
      color: #333;
      p{
        width: 400px;
        white-space: nowrap;
        text-overflow: ellipsis;
        overflow: hidden;
      }
      em{
        color: #ddd;
        float: right;
        margin-right: 20px;
      }
    }
  }
</style>
<style lang="scss" module>
  @import "../../css/element.scss";
  .panel{
    @include panel;
    >h4{
      display: none;
    }
    margin-top: 100px!important;
    .content{
      height: 72px;
      line-height: 72px;
      padding-left: 178px;
      background: url(//m.jr.jd.com/spe/qyy/main/images/scroll_title_img.png) left top no-repeat
    }
  }
</style>
