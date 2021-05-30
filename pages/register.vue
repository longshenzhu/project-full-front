<template>
  <div class="login-container">
      <el-form class="login-form" :model="form" :rules="rules" ref="registerForm">
          <div class="title-container">
              <img src="/logo.png" alt="logo">
          </div>
          <el-form-item props="email" label="邮箱">
              <el-input v-model="form.email" placeholder="请输入邮箱"></el-input>
          </el-form-item>
          <el-form-item props="captcha" label="验证码" class="captcha-container">
              <div class="captcha">
                  <img :src="code.captcha">
                  <el-input v-model="form.email" placeholder="请输入验证码"></el-input>
              </div>
          </el-form-item>
          <el-form-item props="nickname" label="昵称">
              <el-input v-model="form.nickname" placeholder="请输入昵称"></el-input>
          </el-form-item>
          <el-form-item props="passwd" label="密码">
              <el-input v-model="form.passwd" placeholder="请输入密码"></el-input>
          </el-form-item>
          <el-form-item props="repasswd" label="确认密码">
              <el-input v-model="form.repasswd" placeholder="请再次输入密码"></el-input>
          </el-form-item>
          <el-form-item label=" ">
              <el-button>注册</el-button>
          </el-form-item>
      </el-form>
  </div>
</template>

<script>
export default {
    layout: 'login',
    data(){
        return {
            
            form: {
                email:""
            },
            rules: {
                email:[
                    { require:true, message:"请输入邮箱" },
                    { type:'email', message:"请输入正确的邮箱格式" },
                ]
            }
        }
    },
    methods: {
        updateCaptcha(){
            this.captchaUrl = "/api/captcha?_t=" + new Date().getTime()
        }
    }
}
</script>

<style>
    .login-form{
        width:800px;
        margin:50px auto;
    }
        
</style>