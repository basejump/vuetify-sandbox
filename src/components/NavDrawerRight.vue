<template>
<v-navigation-drawer temporary :right="drawerConfig.right" v-model="drawerConfig.show">
      <v-list>
        <v-list-item>
          <v-list-tile @click.native="navDrawerState.clipped = !navDrawerState.clipped">
            <v-list-tile-action>
              <v-switch v-model="navDrawerState.clipped"></v-switch>
            </v-list-tile-action>
            <v-list-tile-title>Nav Drawer Clipped</v-list-tile-title>
            <v-list-tile-action>
              <v-icon >chrome_reader_mode</v-icon>
            </v-list-tile-action>
          </v-list-tile>
        </v-list-item>

        <v-list-item>
          <v-list-tile @click.native="navDrawerState.dark = !navDrawerState.dark">
            <v-list-tile-action>
              <v-switch v-model="navDrawerState.dark"></v-switch>
            </v-list-tile-action>
            <v-list-tile-title>Nav Drawer Dark</v-list-tile-title>
          </v-list-tile>
        </v-list-item>

        <v-list-item>
          <v-list-tile @click.native="navDrawerState.dense = !navDrawerState.dense">
            <v-list-tile-action>
              <v-switch v-model="navDrawerState.dense"></v-switch>
            </v-list-tile-action>
            <v-list-tile-title>Nav Drawer Dense</v-list-tile-title>
            <v-list-tile-action>
            </v-list-tile-action>
          </v-list-tile>
        </v-list-item>

        <v-list-item>
          <v-list-tile @click.native="toolbarState.fixed = !toolbarState.fixed">
            <v-list-tile-action>
              <v-switch v-model="toolbarState.fixed"></v-switch>
            </v-list-tile-action>
            <v-list-tile-title>Fixed Toolbar</v-list-tile-title>
            <v-list-tile-action>
              <v-icon >web</v-icon>
            </v-list-tile-action>
          </v-list-tile>
        </v-list-item>

        <v-list-item>
          <v-list-tile @click.native="footerState.fixed = !footerState.fixed">
            <v-list-tile-action>
              <v-switch v-model="footerState.fixed"></v-switch>
            </v-list-tile-action>
            <v-list-tile-title>Fixed Footer</v-list-tile-title>
            <v-list-tile-action>
              <v-icon >call_to_action</v-icon>
            </v-list-tile-action>
          </v-list-tile>
        </v-list-item>

        <v-list-item>
          <v-list-tile @click.native="drawerConfig.right = !drawerConfig.right">
            <v-list-tile-action>
              <v-switch v-model="drawerConfig.right"></v-switch>
            </v-list-tile-action>
            <v-list-tile-title>Drawer Side (left/right)</v-list-tile-title>
            <v-list-tile-action>
              <v-icon >compare_arrows</v-icon>
            </v-list-tile-action>
          </v-list-tile>
        </v-list-item>

      </v-list>
    </v-navigation-drawer>
</template>

<script>
export default {
  props: ['navDrawerState', 'drawerConfig','toolbarState','footerState'],
  created() {
    console.log(this)
  }
}
</script>

<style lang="stylus">

</style>
