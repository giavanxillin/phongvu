<template>
  <div class="login">
    <div class = "login-bg">
      <h1 class="shift-right">LOGIN</h1>
    <el-form
      :model="ruleForm"
      status-icon
      ref="ruleForm"
      label-width="120px"
      class="ruleForm"
      @submit.native.prevent="signin"
    >
      <el-form-item  prop="username">
        <el-input class="login-input" suffix-icon="el-icon-user"  placeholder="USERNAME" v-model="ruleForm.username"></el-input>
      </el-form-item>

       <el-form-item  prop="password">
        <el-input class="login-input" suffix-icon="el-icon-unlock" type="password" placeholder="PASSWORD" v-model="ruleForm.password"></el-input>
      </el-form-item>
      
      <el-form-item>
        <el-button class = "login-button" @click="signin">LOGIN</el-button>
      </el-form-item>
    </el-form>
    <router-link to="/signup" class="submit">To Register New Account - Click Here</router-link>
    </div>
    

  </div>
</template>

<script>
export default {
  data() {
    return {
      ruleForm: {
        username: "",
        password: ""
      }
    };
  },
  methods: {
    submitForm(formName) {
      this.$refs[formName].validate(valid => {
        if (valid) {
          alert("submit!");
        } else {
          console.log("error submit!!");
          return false;
        }
      });
    },
    async signin(){
      try {
        // await this.$store.dispatch("signIn", this.ruleForm.username);
        this.$router.push('/');
      }
      catch (err){
        console.log(err);
      }
    }
  }
};
</script>

<style scoped>
  .el-input{
    width : 80%;
  }
  .shift-right{
    margin: 0px;
    color: rgb(231, 225, 225);
    font-weight: 500;
    letter-spacing: 3px;
    padding: 30px 10px;
  }
  .login-bg {
    margin: 0 auto;
    width: 38%;
    background-color: rgba(19, 18, 18, 0.6);
    position: absolute;
    right: 50%;
    bottom: 50%;
    transform: translateX(50%) translateY(50%);
  }
  .login{
    background: url(../assets/login-bg.jpg);
    height: 100vh;
    background-position: center;
    background-size: cover;
    position: relative
  }
  .login-button {
    padding: 12px 70px;
    background-color: #537b35;
    border-color : #537b35;
    letter-spacing: 1px;
    font-size: 18px;
    color: white;
  }

  .login-button:hover{
    background-color: white;
    color: #537b35
  }

  .submit {
    color: rgb(231, 225, 225);
    font-weight: 500;
    letter-spacing: 3px;
  }
</style>

<style >
  .login-bg .el-icon-user:before{
      font-size: 30px !important;
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      right: 50%;
  } 
  .login-bg .el-icon-unlock:before{
      font-size: 30px !important;
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      right: 50%;
  }
  .login-bg .el-form-item__label{
  color: rgb(231, 225, 225);  
  letter-spacing: 2px;
  }
  .login-bg .el-form-item__content{
    margin: 0 !important;
    padding: 10px 0;
  }
  .login-input .el-input__inner {
  background-color: transparent ;
  padding: 25px 15px;
  color: white;
  border : 3px solid  #537b35
  }
  .login-input .el-input__inner:hover {
  border : 3px solid  #537b35

  }
  .login-input.is-active .el-input__inner, .el-input__inner:focus {
    border : 3px solid  #537b35;
    outline: 0;
  }

</style>