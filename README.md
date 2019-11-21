# sidebar-menu-drawer

- [Sidebar Menu Drawer](#sidebar-menu-drawer)
- [Demo](#demo)
- [Quick Installation](#quick-installation)
  - [Install Required Dependencies](#install-required-dependencies)
  - [Install Sidebar Menu Drawer](#install-sidebar-menu-drawer)
  - [Using Component](#using-component)

# Demo
<p style="text-align:center">
<img src="https://images2.imagebam.com/f7/b1/a9/de7aa71325876433.png" alt="sidebar-menu-drawer" />
</p>

# Quick Installation

## Install Optional Dependencies
```
npm install --save font-awesome
```

## Install Sidebar Menu Drawer
```
npm install @satmaxt/sidebar-menu-drawer
```

## Using Component
at ``script`` tag section
```js
import SidebarMenuDrawer from '@satmaxt/sidebar-menu-drawer'

export default {
  data() {
    return {
      show: true,
      ...
    }
  },
  components: {
    SidebarMenuDrawer
  }
}
```

at ``template`` section
```html
<template>
  <div>
    <button @click.prevent="show = true">Show</button>
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
```

At ``style`` section
```scss
@import "~@satmaxt/sidebar-menu-drawer/src/assets/sidebar-menu-drawer";

/* Add this line if you installed font-awesome */
$fa-font-path: "~font-awesome/fonts" !default;
@import '~font-awesome/scss/font-awesome';
```

Done

Coded at Sukabumi by [Satmaxt Developer](https://satmaxt.xyz)