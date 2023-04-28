

<script>

import Header from './components/Header.vue'
import Jumbotron from './components/Jumbotron.vue'
import Main from './components/Main.vue'
import CallToAction from './components/CallToAction.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components:{
    Header,
    Jumbotron,
    Main,
    CallToAction,
    Footer
  }
}
</script>

<template>

  <Header/> 

  <Jumbotron/> 

  <Main/> 

  <CallToAction/>

  <Footer/> 

</template>


<style lang="scss">

@use './scss/main.scss'

</style>