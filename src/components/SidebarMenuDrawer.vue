<template>
  <div @click.prevent="hideDrawer" class="sidebar-menu-drawer" :class="{'sidebar-shown': value}">
    <transition name="slide-fade" mode="out-in">
      <div v-show="value" class="sidebar-menu-drawer__body">
        <header class="sidebar-menu-drawer__header">
          <slot name="header" />
        </header>
        <section class="sidebar-menu-drawer__menu">
          <slot/>
        </section>
      </div>
    </transition>
  </div>
</template>

<script>
  export default {
    props: {
      value: {
        type: Boolean,
        required: true
      }
    },
    data() {
      return {
        show: this.value
      }
    },
    methods: {
      hideDrawer() {
        this.$emit('input', false)
      }
    }
  }
</script>

<style lang="scss">
@import '../assets/sidebar-menu-drawer';
</style>