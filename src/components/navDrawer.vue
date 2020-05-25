<template>
    <v-navigation-drawer
      v-model="navDrawer.drawer"
      app
      color="white"
    >
      <v-list dense>
        <v-list-item @click.stop="navDrawer.drawer = !navDrawer.drawer">
          <v-list-item-action>
            <v-icon style="color: black">fas fa-home</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title style="color: black">Home</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
</template>

<script>
import { mapState } from 'vuex';

export default {
    name: 'navDrawer',
    computed: {
        ...mapState(['navDrawer'])
    }
}
</script>

<style>

</style>