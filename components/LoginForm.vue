<template>
  <div>
    <input type="text" name="username" v-model="username">
    <br>
    <input type="password" name="password" v-model="password">
    <br>
    <button @click="handleLoginClick()">Login</button>
  </div>
</template>

<script>
    export default {
      data(){
        return{
          username : "pumiphat",
          password : "123456"
        }
      },
      methods:{
        handleLoginClick(){
          console.log('component',this.username,this.password)
          this.$emit('login-submitted',this.username,this.password)
        }
      }
    }
</script>

<style scoped>

</style>
