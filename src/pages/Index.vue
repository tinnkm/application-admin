<template>
  <div class="layout">
    <i-layout>
      <i-header>
        <i-menu mode="horizontal" theme="dark" active-name="1">
          <div class="layout-logo"></div>
          <div class="layout-nav">
            <i-menu-item name="1">
              <i-icon type="ios-navigate"></i-icon>
              Item 1
            </i-menu-item>
            <i-menu-item name="2">
              <i-icon type="ios-keypad"></i-icon>
              Item 2
            </i-menu-item>
            <i-menu-item name="3">
              <i-icon type="ios-analytics"></i-icon>
              Item 3
            </i-menu-item>
            <i-menu-item name="4">
              <i-icon type="ios-paper"></i-icon>
              Item 4
            </i-menu-item>
          </div>
        </i-menu>
      </i-header>
      <i-layout>
        <Sider class="sider-wrapper" hide-trigger >
          <i-menu active-name="1-2" theme="light" width="auto" :open-names="['1']">
            <i-submenu name="1">
              <template slot="title">
                <i-icon type="ios-navigate"></i-icon>
                Item 1
              </template>
              <i-menu-item name="1-1">Option 1</i-menu-item>
              <i-menu-item name="1-2">Option 2</i-menu-item>
              <i-menu-item name="1-3">Option 3</i-menu-item>
            </i-submenu>
            <i-submenu name="2">
              <template slot="title">
                <i-icon type="ios-keypad"></i-icon>
                Item 2
              </template>
              <i-menu-item name="2-1">Option 1</i-menu-item>
              <i-menu-item name="2-2">Option 2</i-menu-item>
            </i-submenu>
            <i-submenu name="3">
              <template slot="title">
                <i-icon type="ios-analytics"></i-icon>
                Item 3
              </template>
              <i-menu-item name="3-1">Option 1</i-menu-item>
              <i-menu-item name="3-2">Option 2</i-menu-item>
            </i-submenu>
          </i-menu>
        </Sider>
        <i-layout :style="{padding: '0 24px 0 24px'}">
          <Breadcrumb :style="{margin: '24px 0'}">
            <BreadcrumbItem>Home</BreadcrumbItem>
            <BreadcrumbItem>Components</BreadcrumbItem>
            <BreadcrumbItem>Layout</BreadcrumbItem>
          </Breadcrumb>
          <div class="content-wrapper">
            <div class="content">
              <i-content class="content-item">
                Content
              </i-content>
            </div>
            <Footer></Footer>
          </div>
        </i-layout>
      </i-layout>
    </i-layout>
  </div>
</template>

<script>
import Footer from '@/components/Footer'
export default {
  name: 'Index',
  components: {
    Footer
  },
  data () {
    return {
      isCollapsed: false
    }
  },
  computed: {
    rotateIcon () {
      return [
        'menu-icon',
        this.isCollapsed ? 'rotate-icon' : ''
      ]
    },
    menuitemClasses () {
      return [
        'menu-item',
        this.isCollapsed ? 'collapsed-menu' : ''
      ]
    }
  },
  methods: {
    collapsedSider () {
      this.$refs.side.toggleCollapse()
    }
  }
}
</script>

<style scoped>
  .content-wrapper{
    width: 100%;
    display: flex;
    /* css3新单位vh表示屏幕高度 */
    /*min-height: 80vh;*/
    flex-direction: column;
  }
  .content{
    flex: 1;
  }
  .content-item{
    padding: 24px;
    min-height: 81vh;
    background: white;
  }
  .sider-wrapper{
    background: white;
    /*min-height: 93.5vh;*/
  }
  .layout{
    border: 1px solid #d7dde4;
    background: #f5f7f9;
    position: relative;
    border-radius: 4px;
    overflow: hidden;
  }
  .layout-logo{
    width: 100px;
    height: 30px;
    background: #5b6270;
    border-radius: 3px;
    float: left;
    position: relative;
    top: 15px;
    left: 20px;
  }
  .layout-nav{
    width: 420px;
    margin: 0 auto;
    margin-right: 20px;
  }
  .menu-item span{
    display: inline-block;
    overflow: hidden;
    width: 69px;
    text-overflow: ellipsis;
    white-space: nowrap;
    vertical-align: bottom;
    transition: width .2s ease .2s;
  }
  .menu-item i{
    transform: translateX(0px);
    transition: font-size .2s ease, transform .2s ease;
    vertical-align: middle;
    font-size: 16px;
  }
  .collapsed-menu span{
    width: 0px;
    transition: width .2s ease;
  }
  .collapsed-menu i{
    transform: translateX(5px);
    transition: font-size .2s ease .2s, transform .2s ease .2s;
    vertical-align: middle;
    font-size: 22px;
  }
</style>
