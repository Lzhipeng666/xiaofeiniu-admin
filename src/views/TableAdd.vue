<template>
  <div class="">
    <el-breadcrumb>
      <el-breadcrumb-item to="/main">首页</el-breadcrumb-item>
      <el-breadcrumb-item>桌台管理</el-breadcrumb-item>
      <el-breadcrumb-item>添加桌台</el-breadcrumb-item>
    </el-breadcrumb>
    <br>
    <br>
    <br>
    桌台编号:
    <el-input v-model="input1" :disabled="true" style="width:100px"></el-input>
    自动生成,无需赋值
    <br>
    <br>
    桌台别名:
    <el-input v-model="input" style="width:800px" placeholder="给桌台起个吉利喜庆的名字吧"></el-input>
    <br>
    <br>
    桌台类型:
    <el-input v-model="input" style="width:800px" placeholder="桌台类型"></el-input>
    <br>
    <br>
    初始状态:
    <el-radio-group v-model="radio2">
    <el-radio :label="2">空闲</el-radio>
    <el-radio :label="4">预定</el-radio>
    <el-radio :label="6">占用</el-radio>
    <el-radio :label="8">其他</el-radio>
  </el-radio-group>
  </div>
</template>


<script>
  export default {
    data () {
      return {
        radio2: 3
      };
    }
  }
</script>
