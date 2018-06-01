<template>
  <div class='login-wrapper'>
    <div class="login-form">
      <login-form></login-form>
    </div>
  </div>
</template>

<script>
import LoginForm from '@/components/LoginForm'
export default {
  name: 'Login',
  components: {
    LoginForm
  }
}
</script>

<style scoped>
.login-wrapper{
  width: 100%;
  height: 92vh;
  position: relative;
  /*text-align: center;*/
}
.login-form{
  position: absolute;
  top: 50%;
  left: 50%;
  margin-left: -175px;
  margin-top: -150px;
}
</style>
