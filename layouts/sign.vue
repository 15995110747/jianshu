<template>
  <div id="sign-template">
    <nuxt/>
  </div>
</template>

<script>
export default {};
</script>

<style>
body {
  background-color: #f1f1f1;
}
.sign {
  height: 100%;
  font-size: 14px;
  text-align: center;
  min-height: 750px;
}
.sign:before {
  content: "";
  height: 15%;
  width: 100%;
  display: inline-block;
  vertical-align: middle;
}
.sign .logo {
  position: absolute;
  top: 50px;
  left: 50px;
}
.sign img {
  width: 100px;
}
.sign .main {
  width: 400px;
  margin: 50px auto 0;
  padding: 50px 50px 30px;
  background-color: #fff;
  border-radius: 4px;
  box-shadow: 0 0 8px rgba(0, 0, 0, 0.1);
  display: inline-block;
}
.sign .main .title {
  margin: 0 auto 30px;
  color: #939393;
  font-size: 18px;
}
.sign .main h4 a,
.sign .main h4 b {
  padding: 10px;
  color: #969696;
  font-weight: 400;
}
.sign .main h4 b {
  font-weight: 900;
}
.sign .main h4 a.active {
  font-weight: 700;
  color: #ea6f5a;
  border-bottom: 2px solid #ea6f5a;
}
.sign .main h4 a:hover {
  border-bottom: 2px solid #ea6f5a;
  font-weight: 700;
}
.sign .main form {
  color: #969696;
  margin: 0 0 30px;
}
.sign .main form .input-prepend {
  position: relative;
  width: 100%;
}
.sign .main form .input-prepend input {
  width: 100%;
  height: 50px;
  padding: 4px 12px 4px 35px;
  border: 1px solid #c8c8c8;
  border-radius: 2px;
  background-color: rgb(248, 248, 248);
}
.sign .main form .input-prepend i {
  position: absolute;
  left: 15px;
  top: 15px;
  font-size: 20px;
  color: #969696;
}
.sign .main form .input-prepend:nth-of-type(1) input {
  border-bottom: 0;
  border-radius: 2px 2px 0 0;
}
.sign .main form .input-prepend:nth-of-type(2) input {
  border-radius: 0 0 2px 2px;
}
.sign .main form .input-prepend:nth-of-type(3) input {
  border-radius: 0;
  border-bottom: none;
  position: relative;
}
.sign .main form .input-prepend:nth-of-type(3) a.send-ssm{
    background-color:#42C02E;
    color: white;
    position: absolute;
    right: 5px;
    top: 8px;
    width:100px;
    height: 35px;
    border-radius: 20px;
    text-align: center;
    line-height: 35px;
}
.sign .main form .input-prepend:nth-last-of-type(1) input {
  border-radius: 0 0 2px 2px;
  margin-bottom: 20px;
}
.sign .main form .remember {
  float: left;
  margin: 20px 0;
}
.sign .main form .help {
  float: right;
  margin: 25px 0;
  color: #969696;
}
.sign .main form .help:hover {
  color: #333;
}
.sign .main form button {
  width: 100%;
  margin: 0 0 20px 0;
  padding: 9px 18px;
  text-align: center;
  color: #fff;
  background-color: #3194d0;
  border: none;
  border-radius: 22px;
  font-size: 20px;
}
.sign .main form button:hover {
  background-color: #187cb7;
  cursor: pointer;
}
.sign .main .js-form p{
    font-size: 12px;
    line-height: 20px;
    color: #969696;
}
.sign .main .js-form p:nth-of-type(2){
    margin-bottom: 50px;
}
.sign .main .js-form p:nth-of-type(2) a{
    color: #3194D0;
}
.sign .main .more-sign p {
  position: relative;
  font-size: 14px;
  color: #b8b8b8;
  margin-bottom: 20px;
}
.sign .main .more-sign p::before {
  content: "";
  width: 60px;
  border-bottom: 1px solid #b8b8b8;
  position: absolute;
  right: 20px;
  top: 10px;
}
.sign .main .more-sign p::after {
  content: "";
  width: 60px;
  border-bottom: 1px solid #b8b8b8;
  position: absolute;
  left: 20px;
  top: 10px;
}
.sign .main .more-sign ul {
  margin-bottom: 10px;
}
.sign .main .more-sign ul li {
  display: inline-block;
  color: white;
  margin: 0 10px;
  border-radius: 50%;
}
.sign .main .more-sign ul li a {
  width: 50px;
  height: 5px;
  line-height: 50px;
  display: block;
}
.sign .main .more-sign ul li a i {
  font-size: 24px;
}
.sign .main .more-sign ul li i.fa-weixin {
  color: #00bb29;
}
.sign .main .more-sign ul li i.fa-weibo {
  color: #e05244;
}
.sign .main .more-sign ul li i.fa-qq {
  color: #498ab5;
}
@media screen and (max-width: 768px) {
  body {
    background-color: white;
  }
  .sign img {
    display: none;
  }
  .sign .main {
    border: none;
    box-shadow: none;
    margin: 0 auto;
  }
  .sign{
      background-color: #fff;
  }
  .sign:before{
      height: 0;
  }
}
</style>
