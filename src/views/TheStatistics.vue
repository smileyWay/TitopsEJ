<template>
  <div>
    <el-row>
      <el-col :span="6">
        <Statistics></Statistics>
      </el-col>
      <el-col :span="6">
        <Statistics></Statistics>
      </el-col>
      <el-col :span="6">
        <Statistics></Statistics>
      </el-col>
      <el-col :span="6">
        <Statistics></Statistics>
      </el-col>
    </el-row>
  </div>
</template>

<script>
  import Statistics from '@/components/Statistics.vue'
  export default {
    components: {
      Statistics
    }
  }
</script>

<style>
</style>
