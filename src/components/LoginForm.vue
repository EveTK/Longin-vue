<template>
  <form class="login_form" action="www.baidu.com" method="post">
    <div class="login_form_r1">
      <div class="login_text">
        <login-textfield label="Firstname" icon="user" />
        <login-textfield label="花名" icon="user"/>
      </div>
    </div>
    <div class="login_form_r2">
      <login-textfield label="邮箱地址" icon="envelope-o" type="email"/>
    </div>
    <div class="login_form_r3">
      <login-textfield label="输入密码" icon="lock" type="password" />
    </div>
    <div class="login_form_r4">
      <login-textfield label="再次输入密码" icon="lock" type="password"/>
    </div>
    <div class="login_form_r5">
      <login-checkbox label="保持登录状态" />
      <label>忘记密码</label>
    </div>
    <div>
      <login-submit />
    </div>
  </form>
</template>
<script>
import LoginTextfield from './LoginTextfield'
import LoginCheckbox from './LoginCheckbox'
import LoginSubmit from './LoginSubmit'

export default {
  components: {
    LoginTextfield,
    LoginCheckbox,
    LoginSubmit
  },
  data(){
    return {
      password: "password",
      emailForm:{
        mailAddress: null
      }
    }
  }
  
}
</script>
<style>
.login_form {
  padding: 20px;
}
.login_form > div {
  padding-bottom: 10px;
  display: flex;
  min-height: 40px;
  justify-content: space-between;
  transition: all 0.6s ease;
}
.login_text {
  display: flex;
  flex: 1;
}
.login_text .login_textfield {
  border-radius: 0;
}
.login_text .login_textfield:first-child {
  border-radius: 2px 0 0 2px;
}
.login_text .login_textfield:last-child {
  border-radius: 0 2px 2px 0;
}
.login__signup .login_form_r5 {
  opacity: 0;
  /* transform: translateY(100%); */
  transition-duration: 0.4s;
}
.login__signup .login_button label:nth-child(2) {
  transform: translateY(-100%);
  opacity: 0;
}
.login__signin .login_form_r1,
.login__signin .login_form_r4 {
  opacity: 0;
  transform: translateY(30%) scale(0.8);
}
.login__signin .login_form_r2,
.login__signin .login_form_r3 {
  transform: translateY(-100%);
}
.login__signin .login_form_r5 {
  transform: translateY(-200%);
}
.login__signin .login_button label:nth-child(3) {
  transform: translateY(100%);
  opacity: 0;
}
</style>
