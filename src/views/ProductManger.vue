<template>
  <div>
    <el-row class="row1">
      <el-col :span="12"  class="r1-c1">
        <el-row class="r1-c1-r1">
          <img src="../assets/productManager/视频文件上传符号.png" on-click="upload"/>
        </el-row>
        <el-row >
          <div class="r1-c1-r2">
            <div class="r1-c1-r2-2">
            <img src="../assets/sellPosition/图片添加框01.png" class="uploadPic"/>
            <img src="../assets/sellPosition/图片添加框01.png" class="uploadPic"/>
            <img src="../assets/sellPosition/图片添加框01.png" class="uploadPic"/>
            </div>
          </div>
        </el-row>
        <el-row class="r1-c1-r3 productDescription" >
          <el-col :span="12"><ProductDetail :price="999" :desc1="0" :desc2="0"> </ProductDetail></el-col>
          <el-col :span="12"><el-input type="textarea" :rows="8" placeholder="请输入内容"  v-model="productDescription" class="productDetail"></el-input></el-col>
        </el-row>
      </el-col>
      <el-col :span="10.5" class="r1-c2">
        <el-row class="r1-c2-r1">[商圈搜索]</el-row>
        <el-row class="r1-c2-r2">
          <el-input placeholder="[输入关键字]" v-model="sq1" class="sq1"></el-input>
          <el-input placeholder="[输入关键字]" v-model="sq2" class="sq1"></el-input>
          <el-input placeholder="[输入关键字]" v-model="sq3" class="sq1"></el-input>
        </el-row>
        <el-row class="r1-c2-r3">[商品搜索]</el-row>
        <el-row class="r1-c2-r4">
          <el-input placeholder="[输入关键字]" v-model="sp1" class="sq1"></el-input>
          <el-input placeholder="[输入关键字]" v-model="sp2" class="sq1"></el-input>
          <el-input placeholder="[输入关键字]" v-model="sp3" class="sq1"></el-input>
        </el-row>
        <el-row class="r1-c2-r5">[商家搜索]</el-row>
        <el-row class="r1-c2-r6">
          <el-input placeholder="[输入关键字]" v-model="sj1" class="sq1"></el-input>
          <el-input placeholder="[输入关键字]" v-model="sj2" class="sq1"></el-input>
          <el-input placeholder="[输入关键字]" v-model="sj3" class="sq1"></el-input>
        </el-row>
        <el-row class="r1-c2-r7">
          <div class="label1"><label >AR效果</label></div>|
          <div class="label1"><label style="font-size: 20px;">直播</label></div>|
          <div class="label1"><label style="font-size: 20px;">商品电商</label></div>
        </el-row>
      </el-col>
    </el-row>
    <el-row class="row2">
      <el-button>启用</el-button>
      <el-button>提交</el-button>
    </el-row>
  </div>
</template>

<script>
import ProductDetail from '@/components/ProductDetail.vue'
export default {
  name: 'ProductManager',
  components: {
    ProductDetail
  },
  data () {
    return {
      productDescription: '',
      sq1: '',
      sq2: '',
      sq3: '',
      sp1: '',
      sp2: '',
      sp3: '',
      sj1: '',
      sj2: '',
      sj3: '',
      label1Type: 'label1',
      label2Type: 'label2',
      label3Type: 'label3'
    }
  },
  methods: {
    upload () {}
  }
}
</script>

<style>
  .row1 {
    width: 1200px;
  }
  .row2 {
    display: flex;
    justify-content: center;
  }
  .r1-c1 {
    height: 600px;
    margin-right: 30px;
  }
  .r1-c2 {
    height: 600px;
    margin-left: 30px;
  }
  .r1-c1-r1 {
    height: 100px;
  }
  .r1-c1-r3 {
    background-image: url('../assets/productManager/商品详情文本框.png');
    height: 203px;
    width: 100%;
  }
  .r1-c1-r2 {
    height: 150px;
    width: 600px;
    overflow:auto;
  }
  .r1-c1-r2-2 {
    width: 1000px;
  }
  .r1-c1-r3 {
    width: 600px;
  }
  .productDescription {
    margin:5px;
    padding-right: 8px;
  }
  .uploadPic {
    height: 100px;
    width: 100px;
  }
  .r1-c2 {
    /* width: 600px; */
  }
  .r1-c2-r1 {
    height: 50px;
    font-size: 30px;
  }
  .r1-c2-r2 {
    height: 80px;
    font-size: 20px;
  }
  .r1-c2-r3 {
    height: 50px;
    font-size: 30px;
  }
  .r1-c2-r4 {
    height: 80px;
    font-size: 20px;
  }
  .r1-c2-r5 {
    height: 50px;
    font-size: 30px;
  }
  .r1-c2-r6 {
    height: 80px;
    font-size: 20px;
  }
  .r1-c2-r7 {
    display: flex;
    flex-direction: row;
    align-items: center;
  }
  .sq1 {
    width: 150px;
    font-size: 20px;
  }
  .label1 {
    border: 1px solid #000000;
    margin: 0 10px 0 10px;
    font-size: 20px;
    width: 150px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .label1Null {
    border: 0px;
    margin: 0 10px 0 10px;
    font-size: 20px;
  }
</style>
