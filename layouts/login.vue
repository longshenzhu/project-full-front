<template>
  <div>
      <!-- <div>导航</div> -->
      <nuxt></nuxt>
      <!-- <div>底部信息</div> -->
  </div>
</template>

<script>
export default {

}
</script>

<style>
    .login-container{
        width: 100%;
        min-height: 100%;
    }
    .login-container .login-form{
        width: 520px;
        padding: 160px 0;
        margin: 0 auto;
        overflow: hidden;
    }
    .login-container .title-container{
        text-align: center;
        margin-bottom: 20px;
    }
    .login-container .title-container img{
        width: 200px;
    }
    .login-container .captcha-container{
        width: 340px;
    }
    .login-container .captcha-container .captcha{
        position: absolute;
        right: -110px;
    }
    .login-container .captcha-container .captcha img{
        width: 90px;
        height: 50px;
        cursor: pointer;
    }

</style>