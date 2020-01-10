<template>
  <div>
    <navbar/>
    <nuxt/>
    <footer class="footer">
      <div class="container">
        <div class="columns">
          <div class="column is-4 has-text-centered is-hidden-tablet">
            <a class="title is-4" href="#">Moffhub Solutions</a>
          </div>
          <div class="column is-4">
            <div class="level">
              <nuxt-link class="level-item" to="/">Home</nuxt-link>
              <nuxt-link class="level-item" to="/about">About</nuxt-link>
              <nuxt-link class="level-item" to="/projects">Projects</nuxt-link>
            </div>
          </div>
          <div class="column is-4 has-text-centered is-hidden-mobile">
            <a class="title is-4" href="/">Moffhub Solutions</a>
          </div>
          <div class="column is-4 has-text-right">
            <div class="level">
              <nuxt-link class="level-item" to="/blog">Blog</nuxt-link>
              <nuxt-link class="level-item" to="/contact">Contact</nuxt-link>
            </div>
          </div>
        </div>
        <p class="subtitle has-text-centered is-6">&copy; 2020 Moffhub Solutions. Since 2015. All right reserved.</p>
      </div>
    </footer>
  </div>
</template>

<script>
  import Navbar from '../components/Navbar'
  // import Footer from "../components/Footer";

  export default {
    components: {
      Navbar,
      // Footer
    }
  }
</script>

<style>
  html {
    font-family: "Source Sans Pro", "Helvetica Neue", Arial, sans-serif;
  }
</style>
