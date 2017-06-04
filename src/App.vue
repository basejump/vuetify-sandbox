<template>
  <v-app>

    <nav-drawer-main :drawerState="drawer" :items="drawerItems"></nav-drawer-main>
    <v-toolbar primary>
      <v-toolbar-side-icon @click.native.stop="drawer.show = !drawer.show"></v-toolbar-side-icon>
      <v-btn icon @click.native.stop="drawer.mini = !drawer.mini">
        <v-icon v-html="drawer.mini ? 'chevron_right' : 'chevron_left'"></v-icon>
      </v-btn>
      <v-btn icon @click.native.stop="drawer.clipped = !drawer.clipped">
        <v-icon>web</v-icon>
      </v-btn>
      <v-btn icon @click.native.stop="footer.fixed = !footer.fixed">
        <v-icon>remove</v-icon>
      </v-btn>
      <v-toolbar-title v-text="title"></v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items>
        <v-toolbar-item>Home</v-toolbar-item>
        <v-toolbar-item>Contact</v-toolbar-item>
      </v-toolbar-items>
      <v-btn icon @click.native.stop="drawerRight.show = !drawerRight.show">
        <v-icon>menu</v-icon>
      </v-btn>
    </v-toolbar>

    <main>
      <v-container fluid>
        <v-slide-y-transition mode="out-in">
          <router-view></router-view>
        </v-slide-y-transition>
      </v-container>
    </main>

    <nav-drawer-right
      :drawer-config="drawerRight"
      :nav-drawer-state="drawer"
      :toolbar-state="toolbar"
      :footer-state="footer"
    ></nav-drawer-right>


    <v-footer :fixed="footer.fixed">
      <span>&copy; 2017</span>
    </v-footer>
  </v-app>
</template>

<script>
import NavDrawerMain from './components/NavDrawerMain.vue'
import NavDrawerRight from './components/NavDrawerRight.vue'

export default {
  components: {NavDrawerMain, NavDrawerRight},
  data () {
    return {
      title: 'Samples',
      theme: { dark: false },
      drawer: {
        show: true,
        clipped: false,
        mini: false,
        dark: false, //this is the color as in the text color
        persistent: true,
        dense: false
      },
      toolbar: { fixed: false },
      footer: {fixed: false},
      drawerRight: { show: false, right: true },
      drawerItems: [
        {
          title: 'Home',
          action: 'home', //the icon for the action
          group: 'home', //this group has to match the start of the href somehow
          href: '/'
        },
        { divider: true, inset: false },
        { header: 'Component acid tests'},
        {
          title: 'Examples',
          action: 'info',
          href: '/pages/examples'
        },
        {
          title: 'About',
          action: 'info',
          group: 'about',
          items: [
            { href: '/about', title: 'Summary', action: 'computer' },
            { href: '/about/history', title: 'History', action: 'router' }
          ]
        }

      ]
    }
  }
}
</script>

<style lang="stylus">
  @import './stylus/main'
</style>
