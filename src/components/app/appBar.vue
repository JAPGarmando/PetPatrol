<template>
  <v-app-bar
      app
      clipped-right
      color="transparent"
      class="appBar"
      dark
    >
        <v-app-bar-nav-icon @click.stop="navDrawer.drawer = !navDrawer.drawer">
            <v-icon>fas fa-bars</v-icon>
        </v-app-bar-nav-icon>
        <v-spacer></v-spacer>
        <div class="logo"></div>
        <v-spacer></v-spacer>
        <v-app-bar-nav-icon>
            <v-icon>fas fa-search</v-icon>
        </v-app-bar-nav-icon>
    </v-app-bar>
</template>

<script>
import { mapState } from 'vuex'

export default {
    name: 'appBar',
    computed: {
        ...mapState(['navDrawer'])
    }
}
</script>

<style scoped>
    .appBar{
        background-color: transparent;
        border-bottom: white 1px;  
    }
    .logo{
        width: 200px;
        height: 72.64px;
        padding: 0px;
        background-size: contain;
        background-image: url('../../assets/logoPetPatrol.png');
    }
</style>