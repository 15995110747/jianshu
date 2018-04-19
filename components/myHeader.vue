<template>
  <div>
    <nav class="navbar navbar-fixed-top">
      <div class="width-limit">
          <nuxt-link to='/' class="logo">
            <img src="../assets/image/nav-logo.png" alt="">
          </nuxt-link>
          <nuxt-link to='/write' class="write-btn">
            <i class="fa fa-edit"></i>
            写文章          
          </nuxt-link>
          <div class="user" @mouseleave="dropOut()">
            <div class="drop-down" @mouseover="dropOver()">
              <nuxt-link to='/u/123' class="avator">
                <img src="../assets/image/default-avator.jpg" alt="">
              </nuxt-link>
            </div>
            <ul class="drop-menu" v-show="dropShow">
              <li>
                <nuxt-link to='/'>
                  <i class="fa fa-home fa-fw"></i>
                  我的主页
                </nuxt-link>
              </li>
              <li>
                <nuxt-link to='/users/123/like'>
                  <i class="fa fa-heart fa-fw"></i>
                  喜欢的文章
                </nuxt-link>
              </li>
              <li>
                <nuxt-link to='/bookmarks'>
                  <i class="fa fa-bookmark fa-fw"></i>
                  收藏的文章
                </nuxt-link>
              </li>
              <li>
                <nuxt-link to='/settings/basic'>
                  <i class="fa fa-cog fa-fw"></i>
                  设置
                </nuxt-link>
              </li>
              <li>
                <nuxt-link to='/logout'>
                  <i class="fa fa-sign-out fa-fw"></i>
                  退出
                </nuxt-link>
              </li>
            </ul>
          </div>
      </div>
    </nav>
  </div>
</template>
<script>
export default {
  name: "myHeader",
  data(){
    return{
      dropShow:false
    }
  },
  methods:{
    dropOver(){
      this.dropShow=true;
    },
    dropOut(){
      this.dropShow=false;
    }
  }
};
</script>
<style scoped>
nav {
  width: 100%;
  height: 56px;
}
.navbar {
  margin-bottom: 20px;
  border-width: 0 0 1px;
  border-color: #f0f0f0;
}
.navbar:before {
  display: table;
  content: "";
}
.navbar-fixed-top {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 10000;
}
nav .width-limit {
  min-width: 768px;
  max-width: 1440px;
  margin: 0 auto;
  height: 56px;
  /* background-color: black; */
}
nav .logo {
  float: left;
  height: 56px;
}
nav .logo img {
  height: 100%;
}
nav .write-btn {
  float: right;
  width: 100px;
  height: 40px;
  line-height: 40px;
  margin: 8px 15px 0;
  border-radius: 20px;
  font-size: 15px;
  color: #fff;
  background-color: #ea6f5a;
  text-align: center;
}
nav .write-btn:hover {
  background: #ec6149;
  cursor: pointer;
}
nav .user {
  position: relative;
  float: right;
}
nav .user .avator {
  position: relative;
  display: block;
  width: 40px;
  height: 40px;
  margin: 8px 10px 8px 25px;
  display: inline-block;
}
nav .user:hover{
  background-color: #f5f5f5;
}
nav .user .drop-menu li a:hover{
  background-color: #f5f5f5;
}
nav .user .avator:before {
  content: "";
  position: absolute;
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-top: 5px solid #999;
  right: -14px;
  top: 18px;
}
nav .user .avator img {
  width: 100%;
  height: 100%;
  border-radius: 50%;
  border: 1px solid #ccc;
}
nav .user .drop-menu {
  box-shadow: 0 0 8px rgba(0, 0, 0, 0.1);
  position: absolute;
  left: 0;
  min-width: 160px;
  z-index: 10000;
  margin: 0;
  background: #fff;
  padding: 10px 0;
  font-size: 15px;

}
nav .user .drop-menu li a{
  padding: 10px 20px;
  display: block;
  line-height: 30px;
}
nav .user .drop-menu li a i{
  margin-right: 15px;
  color:#ea6f5a;
  font-size: 18px;
}
</style>

