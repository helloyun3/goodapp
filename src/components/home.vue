
<template>
  <div>
    <x-header> good luck ！</x-header>
    <swiper loop auto :list="demo06_list" :index="demo06_index" @on-index-change="demo06_onIndexChange"></swiper>
    <tabbar>
      <tabbar-item>
        <img slot="icon" src="../assets/home.png">
        <span slot="label">home</span>
      </tabbar-item>
      <tabbar-item show-dot>
        <img slot="icon" src="../assets/back.png">
        <span slot="label">back</span>
      </tabbar-item>
      <tabbar-item selected link="/component/demo">
        <img slot="icon" src="../assets/book.png">
        <span slot="label">map</span>
      </tabbar-item>
      <tabbar-item badge="2">
        <img slot="icon" src="../assets/mine.png">
        <span slot="label">mine</span>
      </tabbar-item>
    </tabbar>
  </div>
</template>
<script>
import { Tabbar, TabbarItem, Group, Cell, XHeader, Swiper } from 'vux'
const baseList = [{
  url: 'javascript:',
  img: 'https://ww1.sinaimg.cn/large/663d3650gy1fq66vvsr72j20p00gogo2.jpg',
  title: '送你一朵fua'
}, {
  url: 'javascript:',
  img: 'https://ww1.sinaimg.cn/large/663d3650gy1fq66vw1k2wj20p00goq7n.jpg',
  title: '送你一辆车'
}, {
  url: 'javascript:',
  img: 'https://static.vux.li/demo/5.jpg', // 404
  title: '送你一次旅行',
  fallbackImg: 'https://ww1.sinaimg.cn/large/663d3650gy1fq66vw50iwj20ff0aaaci.jpg'
}]
const urlList = baseList.map((item, index) => ({
  url: 'http://m.baidu.com',
  img: item.img,
  fallbackImg: item.fallbackImg,
  title: `(可点击)${item.title}`
}))
export default {
  components: {
    XHeader,
    Tabbar,
    TabbarItem,
    Group,
    Cell,
    Swiper
  },
  ready () {
  },
  methods: {
  },
  data () {
    return {
      demo06_list: urlList
    }
  }
}
</script>