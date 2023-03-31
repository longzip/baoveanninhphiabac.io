<template>
  <div>
    <Navigation />
    <Nuxt />
    <Footer />
    <a href="#" class="scrollup">Scroll</a>
    <div id="fb-root"></div>
  </div>
</template>

<script>
import Navigation from '~/components/Navigation'
import Footer from '~/components/Footer'
export default {
  components: {
    Navigation,
    Footer,
  },
}
</script>
