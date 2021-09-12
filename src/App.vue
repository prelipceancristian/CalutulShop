<template>
  <v-app style="background-color: rgba(46,64,87);">
    <v-app-bar app :color="constants.mainBlue" dark>
      <v-btn icon @click="isNavigationOpen = !isNavigationOpen">
        <v-icon>mdi-menu</v-icon>
      </v-btn>
      <h1>CalutulBot</h1>
      <v-spacer></v-spacer>
      <User :user="testUser"></User>
    </v-app-bar>
    <v-navigation-drawer app v-model="isNavigationOpen">
    </v-navigation-drawer>
    <v-main :color="black">
      <Tiles />
      
    </v-main>
  </v-app>
</template>

<script>
import Tiles from './components/Tiles'
import { constants } from './common/constants'
import User from './components/User'

export default {
  name: 'App',

  components: {
    Tiles,
    User
  },

  data: () => ({
    isNavigationOpen: false,
    constants: constants,
    testUser: {
      imageURL: '',
      name: 'Chrispy'
    }
  })
}
</script>
