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
            <v-list-item-title><span class="itemTitle">Home</span></v-list-item-title>
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

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
    .itemTitle{
        font-family: 'Poppins',sans-serif;
        font-size: 18px;
        font-weight: bold;
        color: black;
    }
</style>