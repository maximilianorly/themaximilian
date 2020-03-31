<template>
  <div id="app">
    <HeaderBar />
    <Hero />
    <ParallaxBody />
  </div>
</template>

<script>
import HeaderBar from './components/HeaderBar.vue'
import Hero from './components/Hero.vue'
import ParallaxBody from './components/ParallaxBody.vue'

export default {
  name: 'App',
  components: {
    HeaderBar,
    Hero,
    ParallaxBody
  }
}
</script>