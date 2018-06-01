<template>
  <div class='login-wrapper'>
    <div class="login-form">
      <div class='form-wrapper'>
        <i-card class="form-box">
          <div>
            <h3 class="form-title">Welcome!</h3>
            <i-form class="form">
              <i-input>
                <span slot='prepend'><i-icon type='person'></i-icon></span>
              </i-input>
              <br>
              <i-input>
                <span slot='prepend'><i-icon type='locked'></i-icon></span>
              </i-input>
              <br>
              <i-button type='primary' shape='circle' long>登&nbsp;&nbsp;录</i-button>
            </i-form>
          </div>
        </i-card>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LoginForm'
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
  .form-wrapper{
    width: 100%;
    height: 100%;
  }
  .form-box{
    padding: 10px;
    width: 350px;
    height: 300px;
  }
  .form-title{
    margin: 20px 0 20px 0;
    text-align: center;
  }
  .form{
    margin-top: 50px;
  }
</style>
