<template>
  <div class="content-wrapper">
    <div class="content">
      <router-view/>
    </div>
    <Footer></Footer>
  </div>
</template>

<script>
import Footer from '@/components/Footer'
export default {
  name: 'App',
  components: {
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
