<template>
  <v-app>
    <home-design></home-design>
  </v-app>
</template>

<script>
import HomeDesign from './components/HomeDesign';

export default {
  name: 'App',

  components: {
    HomeDesign,
  },

  data: () => ({
    //
  }),
};
</script>
