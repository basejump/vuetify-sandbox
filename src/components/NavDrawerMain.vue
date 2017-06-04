<template>
  <v-navigation-drawer
    :enable-resize-watcher="true"
    v-model="drawerState.show"
    :persistent="drawerState.persistent"
    :mini-variant.sync="drawerState.mini"
    :clipped="drawerState.clipped"
    :dark="drawerState.dark"
  >
  <!-- :dark="drawerState.dark" -->
    <v-list class="pa-0" >
      <v-list-item >
        <v-list-tile avatar tag="div">

          <v-list-tile-avatar>
            <router-link to="/">
              <img src="https://avatars0.githubusercontent.com/u/187726?v=3&s=400">
            </router-link>
          </v-list-tile-avatar>

          <v-list-tile-content class="show-overflow">
            <v-menu transition="v-scale-transition" origin="top">
              <v-list-tile-title slot="activator">
                <span>Joshua Burnett</span> <v-icon>arrow_drop_down</v-icon>
              </v-list-tile-title>
              <v-list >
                <v-list-item>
                  <v-list-tile href="https://github.com/basejump" target="_blank">
                    <v-list-tile-action>
                      <v-icon fa >github</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-title>Github</v-list-tile-title>
                  </v-list-tile>
                </v-list-item>
              </v-list>
            </v-menu>
          </v-list-tile-content>
          <div class="list__tile__action min-width18">
            <v-btn icon small class="pa-0 ma-0"
                   v-on:click.native.stop="drawerState.mini = !drawerState.mini">
              <v-icon class="xs">remove</v-icon>
            </v-btn>
          </div>
          <div class="list__tile__action min-width18">
            <v-btn icon small class="pa-0 ma-0"
                   v-on:click.native.stop="drawerState.show = false">
              <v-icon class="xs">close</v-icon>
            </v-btn>
          </div>
        </v-list-tile>
      </v-list-item>
    </v-list>

    <v-divider ></v-divider>

    <v-list :dense="drawerState.dense">
      <template v-for="(item, i) in items">

        <v-list-group v-if="item.items" :group="item.group" > <!--group header-->

          <v-list-tile avatar slot="item"> <!--group header menu ITEM-->
            <v-list-tile-action>
              <v-icon >{{ item.action }}</v-icon>
            </v-list-tile-action>

            <v-list-tile-content>
              <v-list-tile-title>{{ item.title }}</v-list-tile-title>
            </v-list-tile-content>

            <v-list-tile-action>
              <v-icon >keyboard_arrow_down</v-icon>
            </v-list-tile-action>
          </v-list-tile>

          <!--children submenu-->
          <template v-for="subItem in item.items">

            <v-divider   v-if="subItem.divider" :inset="subItem.inset" ></v-divider>
            <v-subheader v-else-if="subItem.subheader" :inset="subItem.inset" >{{subItem.subheader}}</v-subheader>
            <v-list-item v-else v-bind:key="subItem"> <!--children submenu-->

              <v-list-tile ripple :href="subItem.href"
                           :router="!subItem.target"
                           :disabled="subItem.disabled"
                           :target="subItem.target">

                <v-list-tile-content>
                  <v-list-tile-title>{{ subItem.title }}</v-list-tile-title>
                </v-list-tile-content>

                <v-list-tile-action v-if="subItem.action">
                  <v-icon >{{ subItem.action }}</v-icon>
                </v-list-tile-action>

                <v-list-tile-avatar v-if="subItem.img">
                  <img :src="subItem.img.src" :style="subItem.img.style">
                </v-list-tile-avatar>

              </v-list-tile>

            </v-list-item>
          </template>

        </v-list-group> <!--END group header-->

        <v-subheader  v-else-if="item.header" >{{ item.header }}</v-subheader>
        <v-divider    v-else-if="item.divider"></v-divider>
        <v-list-item  v-else> <!--NO sub menu items, do one without-->

          <v-list-tile avatar ripple :href="item.href" :router="!item.target" :disabled="item.disabled">
            <v-list-tile-action>
              <v-icon>{{ item.action }}</v-icon>
            </v-list-tile-action>

            <v-list-tile-content>
              <v-list-tile-title>{{ item.title }}</v-list-tile-title>
            </v-list-tile-content>

            <v-list-tile-action v-if="item.subAction">
              <v-icon class="success--text">{{ item.subAction }}</v-icon>
            </v-list-tile-action>
          </v-list-tile>

        </v-list-item> <!--end no sub menu items-->

      </template>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  props: ['drawerState', 'items'],
  computed: {
    isDark () { return this.drawerState.dark },
    isActive: {
      get () {
        return true //this.$store.state.sidebar
      },
      set (val) {
        //this.$store.commit('vuetify/SIDEBAR', val)
      }
    }
  },
  created() {
    console.log(this)
  }
}
</script>

<style lang="stylus">

</style>
