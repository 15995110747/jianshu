<template>
  <div class="sign">
      <div class="logo">
          <nuxt-link to='/'>
            <img src="../assets/image/logo.png" alt="">
          </nuxt-link>
      </div>
      <div class="main">
          <div class="title">
              <h4>
              <nuxt-link to='sign-in'>
              登录
              </nuxt-link>
          <b>·</b>
          <nuxt-link to='sign-up' class="active">
              注册
          </nuxt-link>
          </h4>
          </div>
          <div class="js-form">
              <form method="post">
                <div class="input-prepend">
                  <input type="text" placeholder="你的昵称">
                  <i class="fa fa-user"></i>
                  </div>
                  <div class="input-prepend">
                  <input type="text" placeholder="手机号">
                  <i class="fa fa-phone"></i>
                  </div>
                  <div class="input-prepend">
                  <input type="text" placeholder="手机验证码">
                  <i class="fa fa-shield"></i>
                  <a href="#" class="send-ssm">发送验证码</a>
                  </div>
                  <div class="input-prepend">
                  <input type="text" placeholder="设置密码">
                  <i class="fa fa-lock"></i>
                  </div>
                  <button class="sign-up-btn">注册</button>
              </form>
              <p>点击 “注册” 即表示您同意并愿意遵守简书</p>
              <p>
                <nuxt-link to='/'>用户协议</nuxt-link>
                和
                <nuxt-link to='/'>隐私政策</nuxt-link>
              </p>
          </div>
          <div class="more-sign">
              <p>社交账号直接注册</p>
              <ul>
                  <li>
                      <nuxt-link to='/'>
                            <i class="fa fa-weixin"></i>
                      </nuxt-link>
                  </li>
                  <li>
                      <nuxt-link to='/'>
                            <i class="fa fa-qq"></i>
                      </nuxt-link>
                  </li>
              </ul>
          </div>
      </div>
  </div>
</template>
<script>
export default {
  layout: "sign",
  head: {
    title: "简书-注册",
    meta: [
      { name: "keywords", content: "注册页面" },
      { name: "description", content: "注册简书" },
      { name: "Author", content: "chen" },
      { charset: "utf-8" }
    ]
  },
  data() {
    return {};
  }
};
</script>
<style scoped>
.sign .main form .input-prepend:nth-of-type(2) input {
  border-radius: 0;
  border-bottom: 0;
}
.sign .main form{
  margin-bottom: 0;
}
.sign .main form button{
  background-color: #42C02E;
  margin-bottom: 10px;
}
.sign .main form button:hover{
  background-color: #3dba22;
}

</style>




