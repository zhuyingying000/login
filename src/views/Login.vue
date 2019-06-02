<template>
  <div class="container">
    <el-form :model="loginForm" :rules="rules" ref="loginForm">

      <el-form-item class="border-line" prop="username">
        <el-input placeholder="admin@wz.com" v-model="loginForm.username">
          <template slot="prepend"><i class="el-icon-user"></i></template>
        </el-input>
      </el-form-item>


      <el-form-item style="margin-top: 20px;" class="border-line" prop="password">
        <el-input placeholder="Password" v-model="loginForm.password">
          <template slot="prepend"><i class="el-icon-lock"></i></template>
        </el-input>
      </el-form-item>


      <el-button type="primary" @click="submitForm('loginForm')">登录</el-button>
    </el-form>
  </div>
</template>

<style scoped>
  .border-line, .el-button {
    width: 300px;
  }

  .container {
    height: 100%;
    background-image: url("../assets/background.png");
    background-size: 100% 100%;
  }

  .el-form {
    position: relative;
    top: 40%;
    left:40%;

  }

</style>

<script>
  export default {
    data () {
      return {
        loginForm: {
          username: '',
          password: '',

        },
        rules: {
          username: [
            { required: true, message: '请输入活动名称', trigger: 'blur' },
            { min: 3, max: 5, message: '长度在 3 到 5 个字符', trigger: 'blur' }
          ],
          password: [
            { required: true, message: '请输入密码', trigger: 'blur' },
            { min: 6, max: 12, message: '长度在 6 到 12 个字符', trigger: 'blur' }
          ],
        },
      }

    },

    methods: {
      submitForm (formName) {
        this.$refs[formName].validate((valid) => {
          if (valid) {
            alert('submit!')
            setTimeout(()=>{
              this.$router.push('home')
            },1000)
          } else {
            console.log('error submit!!')
            return false
          }
        })
      },

    }

  }
</script>
