<template>
  <v-app>
    <v-main>
      <AppHeader></AppHeader>
    </v-main>
  </v-app>
</template>

<script>
import AppHeader from './components/AppHeader.vue';

export default {
  name: 'App',

  components: {
    AppHeader,
  },

  data: () => ({
    //
  }),
}
</script>
