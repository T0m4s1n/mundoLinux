<template>
  <div id="app">
    <AppHeader />
    <HeroComponent />
    <HomeView />
    <AboutPage />
    <InfoView />
    <QuestionsView />
    <Footer/>
  </div>
</template>

<script>
import HomeView from './components/HomeView.vue';
import HeroComponent from './components/Hero.vue';
import AppHeader from './components/Header.vue';
import AboutPage from './components/About.vue';
import QuestionsView from './components/Questions.vue';
import Footer from './components/Footer.vue';
import InfoView from './components/Info.vue';

export default {
  name: 'App',
  components: {
    HomeView,
    AppHeader,
    HeroComponent,  
    AboutPage,
    QuestionsView,
    Footer,
    InfoView
  }
}

</script>
<style>
#app {
  font-family: 'Poppins', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: black;
  color: #2c3e50;
  margin: 0;
  padding: 0;
  width: 100vw;
  height: 100%;
  overflow-x: hidden;
}

#homeview {
  width: 100vw;
  height: auto;
}

body {
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}

</style>
