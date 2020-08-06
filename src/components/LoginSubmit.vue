<template>
  <span class="login_button">
    <input type="button" value="" />
    <label>登录</label>
    <label>注册</label>
  </span>
</template>
<style>
.login_button {
  position: relative;
  display: flex;
  flex: 1;
  overflow: hidden;
}
.login_button input {
  display: block;
  flex: 1;
  width: 0;
  height: 40px;
  border: none;
  border-radius: 2px;
  outline: none;
  background: #dbac85;
}
.login_button label {
  position: absolute;
  width: 100%;
  height: 100%;
  align-items: center;
  justify-content: center;
  display: flex;
  transition: all 0.6s ease;
}
</style>
