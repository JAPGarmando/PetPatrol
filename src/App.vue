<template>
  <v-app id="app">

    <v-app-bar
      app
      clipped-right
      color="transparent"
      dark
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer">
        <v-icon>fas fa-bars</v-icon>
      </v-app-bar-nav-icon>
    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      app
      clipped
      color="transparent"
    >
      <v-list dense>
        <v-list-item @click.stop="drawer = !drawer">
          <v-list-item-action>
            <v-icon style="color: white">fas fa-home</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title style="color: white">Home</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-content>
    </v-content>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  components: {

  },

  data: () => ({
    drawer: false,
  }),
};
</script>

<style scoped>
.appBar{
  background-color: transparent;
}
#app{
  background-image: linear-gradient(191deg, rgba(35,148,160,1) 44%, rgba(168,180,16,1) 100%);
}
</style>