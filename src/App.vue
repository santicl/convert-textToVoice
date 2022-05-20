<template>
  <div id="app">
    <Header />
    <TextVoiceApp />
    <SectionAboutProyect />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import TextVoiceApp from './components/TextVoiceApp.vue'
import SectionAboutProyect from './components/SectionAboutProyect.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    TextVoiceApp,
    SectionAboutProyect,
    Footer
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
}
</style>
