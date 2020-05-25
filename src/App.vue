<template>
  <v-app id="app">
    <v-app-bar
      app
      clipped-right
      color="transparent"
      class="appBar"
      dark
      flat
      
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer">
        <v-icon>fas fa-bars</v-icon>
      </v-app-bar-nav-icon>
      <v-spacer></v-spacer>
        <div class="logo"></div>
        <v-spacer></v-spacer>
        <v-icon>fas fa-search</v-icon>

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
      <mascotasCard/>
    </v-content>
  </v-app>
</template>

<script>
import mascotasCard from './components/mascotasCard.vue'
export default {
  
  name: 'App',

  components: {
    mascotasCard,
  },

  data: () => ({
    drawer: false,
  }),
};
</script>

<style scoped>
.appBar{
  background-color: transparent;
  border-bottom: white 1px;
  
}
#app{
  background-image: linear-gradient(191deg, rgba(35,148,160,1) 44%, rgba(168,180,16,1) 100%);
}
.logo{
   width: 200px;
   height: 72.64px;
   padding: 0px;
   background-size: contain;
    background-image: url('./assets/logoPetPatrol.png'); 
   /* padding-top: 40px; */
}

</style>