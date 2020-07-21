<template>
  <div>
    <Title :name="this.name"></Title>
    <el-container>
      <el-aside >
        <el-menu default-active="1" @select="handleSelect" class="el-aside">
          <el-menu-item index="1">
            <span slot="title" :class="{active: index==1, normal: !index==1}">导航1</span>
          </el-menu-item>
          <el-menu-item index="2">
						
            <span slot="title" :class="{active: index==2, normal: !index==2}">导航2</span>
          </el-menu-item>
          <el-menu-item index="3">
            <span slot="title" :class="{active: index==3, normal: !index==3}">导航3</span>
          </el-menu-item>
          <el-menu-item index="4">
            <span slot="title" :class="{active: index==4, normal: !index==4}">统计</span>
          </el-menu-item>
        </el-menu>
      </el-aside>
      <el-main class="el-main">
        <template>
          <router-view/>
        </template>
      </el-main>
    </el-container>
  </div>
</template>

<script>
import Title from '@/components/title/index.vue'

export default {
  name: 'Home',
  components: {
    Title
  },
  data () {
    return {
      isActive: false,
      index: 0,
      name: '视频博主管理后台'
    }
  },
  methods: {
    handleSelect (index, indexPath) {
      this.index = index
      if (index === '1') {
        this.$router.push('/productlist')
      } else if (index === '2') {
        this.$router.push('/viewtest')
      } else if (index === '3') {
        this.$router.push('/productmanager')
      } else if (index === '4') {
        this.$router.push('/TheStatistics')
      }
      console.log(index, indexPath)
    }
  }
}
</script>
<style>
.active {
  font-size: 40px;
  color: black;
}
.normal {
  font-size: 15px;
  color: black;
}
.el-aside {
  width: 200px;
}
</style>
