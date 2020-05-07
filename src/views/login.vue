<template>
  <div class="home">
    <el-row style="height: 90px; margin-bottom: 100px;" class="bottom">
      <el-col :span="9"><div><img src="@/assets/Home/NUTUBE的logo.png" style="object-fit: contain"/></div>
      </el-col>
      <el-col :span="2" ><div style="justify-content: start; display: flex; padding-left: 15px;"><img src="../assets/Home/间隔号.png" /></div>
      </el-col>
      <el-col :span="9"><span class="row1-col3-text">自由的视频交互平台</span>
      </el-col>
      <el-col :span="6" ><div class="row1-col4-text">视频博主管理后台</div>
      </el-col>
    </el-row>
    <el-row class="el-row2">
      <el-col :span="7" style="min-height: 30px;"><div ></div></el-col>
      <el-col :span="8"><el-input v-model="phone" placeholder="手机号"/></el-col>
      <el-col :span="9"><div></div></el-col>
    </el-row>
    <el-row class="el-row3">
      <el-col :span="7" style="min-height: 30px;"><div></div></el-col>
      <el-col :span="8"><el-input v-model="identifyCode" placeholder="验证码"/></el-col>
      <el-col :span="9"><el-button type="text" style="font-size: 25px;color: black">获取验证码</el-button></el-col>
    </el-row>
    <el-row class="el-row4">
      <el-col :span="7" style="min-height: 30px;"></el-col>
      <el-col :span="8"><el-button type="text"><span style="font-size: 40px; color: black">登 录</span></el-button></el-col>
      <el-col :span="9" style="min-height: 30px"></el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'Login'
}
</script>
<style>
body {
  background-color: rgb(232, 233, 230);
}
.el-row3 {
  margin-bottom: 40px;
}
.el-row2 {
  margin-bottom: 20px;
}
.home {
  background-color: rgb(232, 233, 230);
  padding: 20px;
}
.home div {
  --flex: 1;
}
input {
  max-width: 300px;
}
img {
    max-width: 100%;
    max-height: 90px;
}
.image {
    display: block;
  }
  .bottom {
    align-items: flex-end ;
    display: flex;
  }
.row1-col3-text {
  text-align: start;
  font-family: SourceHanSansCN-Normal;
  font-weight: bold;
  font-size: 35px;
}
.row1-col4-text {
  text-align: end;
  font-family: SourceHanSansCN-Normal;
  font-weight: bold;
  font-size: 17px;
}
</style>
