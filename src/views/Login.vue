<template>
  <div class="login">
    <el-card class="xfn-login-card">
      <div slot="header">管理员登录</div>
      <div>
        <el-form label-width="100px">
          <el-form-item label="管理员名：">
            <el-input v-model="formData.aname" placeholder="请输入管理员名"></el-input>
          </el-form-item>
          <el-form-item label="登录密码：">
            <el-input type="password" v-model="formData.apwd" placeholder="请输入管理员密码"></el-input>
          </el-form-item>
          <el-form-item>
            <el-button type="primary" @click="doLogin">登录</el-button>  
            <el-button @click="doCancel">取消</el-button>
          </el-form-item>
        </el-form>
      </div>
    </el-card>
  </div>
</template>

<script>
  export default {
    data(){   //普通组件的模型数据是函数返回值
      return {
        formData:{
          aname:'',
          apwd:''
        }
      }
    },
    methods:{
      doLogin(){  //执行登录
        var url=this.$store.state.adminName
        this.$axios.get(this.$store.state.adminName)
      },
      doCancel(){ //清除用户的输入

      }
    }
  }
</script>

<style lang="scss">
  .xfn-login-card{
    width:450px;
    margin:150px auto;

    .el-card__header{
      text-align:center;
      font-size:1.2em;
    }
  }
</style>
