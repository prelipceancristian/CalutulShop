<template>
  <v-app>
    <v-app-bar
      app
      color="blue"
      dark
    >
      CalutulShop
    </v-app-bar>

    <v-main>
      <HelloWorld/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import {constants} from './common/constants'

export default {
  name: 'App',
  constants: constants,

  components: {
    HelloWorld,
  },

  data: () => ({
    //
  }),
};
</script>
