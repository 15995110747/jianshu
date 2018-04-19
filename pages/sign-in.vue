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
              <nuxt-link class="active" to='sign-in'>
              登录
              </nuxt-link>
          <b>·</b>
          <nuxt-link to='sign-up'>
              注册
          </nuxt-link>
          </h4>
          </div>
          <div class="js-form">
              <form method="post">
                  <div class="input-prepend">
                  <input type="text" placeholder="手机号或邮箱">
                  <i class="fa fa-user"></i>
                  </div>
                  <div class="input-prepend">
                  <input type="text" placeholder="密码">
                  <i class="fa fa-lock"></i>
                  </div>
                  <div class="remember">
                  <input type="checkbox">
                  <span>记住我</span>
                  </div>
                  <nuxt-link class="help" to='/'>登录遇到问题?</nuxt-link>
                  <button class="sign-in-btn">登录</button>
              </form>
          </div>
          <div class="more-sign">
              <p>社交账号登录</p>
              <ul>
                  <li>
                      <nuxt-link to='/'>
                            <i class="fa fa-weixin"></i>
                      </nuxt-link>
                  </li>
                  <li>
                      <nuxt-link to='/'>
                            <i class="fa fa-weibo"></i>
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
  // 设置页面的标题以及描述，关键字等信息
  // 修改当前页面的默认模板为sign.vue
  // 如果不写的话，默认是default.icon
  layout: "sign",
  head: {
    title: "简书-登录",
    meta: [
      { name: "keywords", content: "登录页面" },
      { name: "description", content: "登陆简书" },
      { name: "Author", content: "chen" },
      { charset: "utf-8" }
    ]
  },
  data() {
    return {};
  }
};
</script>


