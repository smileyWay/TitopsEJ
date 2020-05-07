<template>
  <div class="product-main">
    <el-row>
      <el-col :span="8" v-for="item in this.productNameList" :key="item.id">
        <SellPosition :img="item.img" :productName="item.productName" :price="item.price" :desc1="item.desc1" :desc2="item.desc2" :desc3="item.desc3" class="product"></SellPosition>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import SellPosition from '@/components/SellPosition.vue'
export default {
  name: 'ProductList',
  components: {
    SellPosition
  },
  created: function () {
    var i = 0
    for (i = 0; i < 10; i++) {
      this.productNameList[i] = {
        img: require('@/assets/sellPosition/01商品位 缩略图 图例.png'),
        productName: '毕莫德蒙精品酒店',
        price: '999',
        desc1: '完整的观景套房体验',
        desc2: '房型:一起居室+2卧式+1卫生间',
        desc3: '规格:总面积76平/主卧室双人大床',
        id: i
      }
    }
    var len = this.productNameList.length
    this.rows = parseInt(len / 3) + 1
    this.colTail = len % 3 + 1
    this.productNameList[i] = {
      img: require('@/assets/sellPosition/图片添加框01.png'),
      productName: ' ',
      price: ' ',
      desc1: ' ',
      desc2: ' ',
      desc3: ' ',
      id: i
    }
  },
  data () {
    return {
      rows: 0,
      colTail: 0,
      productNameList: [],
      img: require('@/assets/sellPosition/01商品位 缩略图 图例.png'),
      productName: '毕莫德蒙精品酒店',
      price: '999',
      desc1: '完整的观景套房体验',
      desc2: '房型:一起居室+2卧式+1卫生间',
      desc3: '规格:总面积76平/主卧室双人大床'
    }
  }
}
</script>

<style>
.product-main {
  min-width: 1200px;
}
.product {
  margin: 20px;
}
</style>
