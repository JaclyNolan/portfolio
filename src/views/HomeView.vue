<template>
  <section class="section" id="home">
    <AppHero></AppHero>
  </section>
  <section class="section" id="about-me">
    <AppAboutMe></AppAboutMe>
  </section>
  <section class="section" id="projects">
    <AppProjects></AppProjects>
  </section>
</template>

<style lang="scss">
#home, #projects {
  background-color: #f9f9f9;
}
</style>

<script>
import AppAboutMe from '@/components/AppAboutMe.vue';
import AppHero from '@/components/AppHero.vue';
import AppProjects from '@/components/AppProjects.vue';

// @ is an alias to /src

export default {
  name: 'HomeView',
  components: { AppHero, AppAboutMe, AppProjects }
}
</script>
