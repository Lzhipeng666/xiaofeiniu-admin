<template>
  <div class="settings">
    <el-breadcrumb>
      <el-breadcrumb-item to="/main">首页</el-breadcrumb-item>
      <el-breadcrumb-item>全局设置</el-breadcrumb-item>
    </el-breadcrumb>

    <br>
    <el-card shadow="never">
      <el-form label-width="110px">
      
        <el-form-item label="应用名称：">
          <el-input v-model="formData.appName"></el-input>
        </el-form-item>

        <el-form-item label="数据API地址：">
          <el-input v-model="formData.apiUrl"></el-input>
        </el-form-item>

        <el-form-item label="管理后台地址：">
          <el-input v-model="formData.adminUrl"></el-input>
        </el-form-item>

        <el-form-item label="客户App地址：">
          <el-input v-model="formData.appUrl"></el-input>
        </el-form-item>

        <el-form-item label="ICP备案号：">
          <el-input v-model="formData.icp"></el-input>
        </el-form-item>

        <el-form-item label="版权声明：">
          <el-input v-model="formData.copyright"></el-input>
        </el-form-item>

        <el-form-item>
          <el-button type="primary">提交</el-button>
          <el-button>取消</el-button>
        </el-form-item>
      </el-form>
    </el-card>
  </div>
</template>

<script>
export default {
  data(){
    return {
      formData:{ }
    }
  },
  mounted(){
    //将$store存储中的全局配置数据赋值给中间变量-formData，方便表单元素执行双向数据绑定
    this.formData = this.$store.state.globalSettings;
  }
}
</script>
