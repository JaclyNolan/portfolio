<template>
  <section class="section" id="home">
      <AppHero></AppHero>
  </section>
  <section class="section" id="about-me">
    
  </section>
</template>

<style lang="scss">
.section {
  gap: 7rem;
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
