<template>
  <section id="home">
    <v-sheet id="home-sheet" color="#f9f9f9" height="100vh">
      <AppHero></AppHero>
    </v-sheet>
  </section>
</template>

<style lang="scss">
#home-sheet {
  display: flex-start;
  justify-content: center;
  padding: 5rem 0;
}
</style>

<script>
import AppHero from '@/components/AppHero.vue';

// @ is an alias to /src

export default {
  name: 'HomeView',
  components: { AppHero }
}
</script>
