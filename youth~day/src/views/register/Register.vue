<template>
  <div class="bj">
    <div class="register">
      <img src="~assets/img/common/logo.svg" alt="">
    </div>
    <div class="input">
      <input type="text" placeholder="请输入账号">
    </div>  
      <div class="input">
        <input type="password" placeholder="请输入密码">
      </div>
     <div class="btn">
        <button>注册</button>
     </div>
       
      
    
  </div>
</template>

<script>
export default {
  name:"Register",

 
}
</script>
<style  scoped>

.register{
  font-size: 30px;
  text-align: center;
  margin: 15%;
}
.input{
  text-align: center;
}
input{
  width: 65%;
  font-family:'宋体';
  box-sizing: border-box;
  border:none;
  padding: 10px;
  border-bottom: 1px solid orangered;
  margin-bottom: 30px;
}
button{
width: 70%;
height: 32px;
border:none;
border-radius: 10px;
background: orangered;
color: #fff
}
.btn{
  width: 100%;
  text-align: center;
  margin-top: 10%;
}
</style>