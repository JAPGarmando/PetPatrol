<template>
  <v-app id="app">

    <application-bar/>

    <navigation-drawer/>

    <v-content>
      <router-view/>
    </v-content>
  </v-app>
</template>

<script>
import { mapState } from 'vuex'
import navigationDrawer from './components/navDrawer.vue'
import applicationBar from './components/appBar.vue'

export default {
  name: 'App',

  components: {
    navigationDrawer,
    applicationBar
  },

  data: () => ({
    drawer: false,
  }),

  computed: {
    ...mapState(['navDrawer'])
  }
};
</script>

<style scoped>
#app{
  background-image: linear-gradient(191deg, rgba(35,148,160,1) 44%, rgba(168,180,16,1) 100%);
}
</style>