<template>
  <!-- todo:目前只是为了方便调试所以才有这个入口，之后入口需改为登陆页，其他页面均通过登陆也作为入口，由其发起跳转 -->
<router-view/>
</template>

<script>

export default {
  name: 'App',
  components: {
    // Footer
  }
}
</script>

<style scoped>

</style>
