
<template>
<div class="demo-input-suffix">
  <el-input
      placeholder="请选择日期"
      suffix-icon="el-icon-date"
      v-model="input1">
  </el-input>
  <el-input
      placeholder="请输入内容"
      prefix-icon="el-icon-search"
      v-model="input2">
  </el-input>
</div>
</template>
<script>
  export default {
    data() {
      return {
        input1: '',
        input2: '',
      }
    }
  }
</script>
<style scoped>
  .el-input{
    width:350px;
    margin-right:15px;
  }
</style>
