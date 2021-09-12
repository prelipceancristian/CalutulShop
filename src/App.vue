<template>
  <v-app style="background-color: rgba(46,64,87);">
    <v-app-bar app dark :color="constants.mainBlue">
      <v-btn icon @click="isNavigationOpen = !isNavigationOpen">
        <v-icon>mdi-menu</v-icon>
      </v-btn>
      <h1>CalutulBot</h1>
      <v-spacer></v-spacer>
      <User :user="testUser"></User>
    </v-app-bar>
    <v-navigation-drawer
      app
      v-model="isNavigationOpen"
      width="300"
      dark
      temporary
      :color="constants.black"
    >
      <NavigationDrawerContent />
    </v-navigation-drawer>
    <v-main>
      <Tiles />
    </v-main>
  </v-app>
</template>

<script>
import Tiles from './components/Tiles'
import { constants } from './common/constants'
import User from './components/User'
import NavigationDrawerContent from './components/NavigationDrawerContent'

export default {
  name: 'App',

  components: {
    Tiles,
    User,
    NavigationDrawerContent
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
