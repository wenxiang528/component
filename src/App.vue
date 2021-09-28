<template>
  <div id="app">
    <img src="./assets/logo.png">
    <div>
      <el-button @click="startHacking">Start</el-button>
    </div>
    <header-div :logo="logoMsg"></header-div>
    <br>
    <br>
    <login-div @transferUser="getUser"></login-div>
    <p>用户名为:{{user}}</p>
  </div>
</template>

<script>
import HeaderDiv from "~/components/header";
import loginDiv from "./views/login"
export default {
  components: {
    HeaderDiv,
    loginDiv,
  },
  data(){
    return{
      logoMsg:'WiseWrong',
      user:''
    }
  },
  methods: {
    startHacking () {
      this.$notify({
        title: 'It works!',
        type: 'success',
        message: 'We\'ve laid the ground work for you. It\'s time for you to build something epic!',
        duration: 5000
      })
    },
    getUser(data){
      this.user=data
    }
  }
}
</script>

<style>
#app {
  font-family: Helvetica, sans-serif;
  text-align: center;
}

</style>
