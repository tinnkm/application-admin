<template>
<div class="content-wrapper">
  <div class="content">
    <login-form></login-form>
  </div>
  <Footer></Footer>
</div>
</template>

<script>
import Footer from '@/components/Footer'
import LoginForm from '@/components/LoginForm'
export default {
  name: 'Login',
  components: {
    LoginForm,
    Footer
  }
}
</script>

<style scoped>
  .content-wrapper{
    width: 100%;
    background: steelblue;
    display: flex;
    /* css3新单位vh表示屏幕高度 */
    min-height: 100vh;
    flex-direction: column;
  }
  .content {
    flex: 1;
  }
</style>
