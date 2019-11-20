<template>
  <div id="app">
    <header class="sidebar-menu-drawer-header">
      <button @click.prevent="show = true" class="burger-menu">
        <i class="fa fa-bars"></i>
      </button>
      <h1 class="title">Sidebar Menu Drawer</h1>
    </header>
    <sidebar-menu-drawer v-model="show">
      <template v-slot:header>
        <h2 class="title">Sidebar Menu</h2>
      </template>
      <ul>
        <li><a href="#"><i class="fa fa-home fa-fw"></i> Home</a></li>
        <li><a href="#"><i class="fa fa-info fa-fw"></i> About</a></li>
        <li><a href="#"><i class="fa fa-envelope fa-fw"></i> Contact</a></li>
        <li><a href="#"><i class="fa fa-lock fa-fw"></i> Privacy</a></li>
        <li class="divider"></li>
        <li><a href="#"><i class="fa fa-tags fa-fw"></i> Product</a></li>
        <li><a href="#"><i class="fa fa-file-text fa-fw"></i> Blog</a></li>
        <li><a href="#"><i class="fa fa-envelope fa-fw"></i> Support</a></li>
      </ul>
    </sidebar-menu-drawer>
  </div>
</template>

<script>
import SidebarMenuDrawer from '@/components/SidebarMenuDrawer.vue';

export default {
  name: 'app',
  data() {
    return {
      show: false
    }
  },
  components: {
    SidebarMenuDrawer
  }
}
</script>

<style lang="scss">
$fa-font-path: "~font-awesome/fonts" !default;
@import '~font-awesome/scss/font-awesome';
@import 'assets/variables';
body {
  margin: 0;
}
#app {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.sidebar-menu-drawer-header {
  background-color: $primary;
  color: #fff;
  display: flex;
  align-items: center;

  button.burger-menu {
    background-color: transparent;
    border: none;
    color: #fff;
    cursor: pointer;
    padding: 26px 32px;
    font-size: 24px;
    outline: none;
    &:active {
      background-color: $hover-bg;
    }
  }

  h1.title {
    font-size: 36px;
    padding-left: 32px;
    margin: 0;
  }
}
</style>
