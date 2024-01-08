<!-- src/components/Header.vue -->
<template>
  <v-app-bar app color="white" :elevation="2" class="px-4">

    <app-logo></app-logo>
    <v-spacer></v-spacer>

    <app-header-nav-button routeName="Home" icon="mdi-home" label="Home" />
    <app-header-nav-button routeName="About" icon="mdi-home" label="About" />
    <app-header-nav-button routeName="About" icon="mdi-home" label="Project" />
    <app-header-nav-button routeName="Home" icon="mdi-home" label="Contact" />


    <!-- <v-navigation-drawer v-model="drawer" app>
        <v-list>
          <v-list-item-group>
            <v-list-item v-for="(item, index) in items" :key="index" @click="goTo(item.route)">
              <v-list-item-action>
                <v-icon>{{ item.icon }}</v-icon>
              </v-list-item-action>
              <v-list-item-content>
                <v-list-item-title>{{ item.title }}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer> -->
  </v-app-bar>
</template>
  
<script>
import AppLogo from './AppLogo.vue'
import AppHeaderNavButton from './AppHeaderNavButton.vue';

export default {
  data() {
    return {
      // drawer: false,
      // items: [
      //   { title: 'Home', icon: 'mdi-home', route: '/' },
      //   { title: 'About', icon: 'mdi-account', route: '/about' },
      //   { title: 'Projects', icon: 'mdi-briefcase', route: '/projects' },
      //   { title: 'Contact', icon: 'mdi-email', route: '/contact' },
      // ],
    };
  },
  methods: {
    //   toggleDrawer() {
    //     this.drawer = !this.drawer;
    //   },
    //   goTo(route) {
    //     this.$router.push(route);
    //     this.drawer = false;
    //   },
  },
  components: { AppHeaderNavButton, AppLogo }
};
</script>
  
<style scoped>
/* Add any custom styling for your header here */
</style>
  