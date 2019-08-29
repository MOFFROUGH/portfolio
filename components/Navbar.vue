<template>
  <nav class="navbar is-light" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
      <img src="~/assets/imgs/mlogo.png" width="100px" height="100px" />
      <h1 class="navbar-item">Moffhub Solutions</h1>
      <a
        role="button"
        class="navbar-burger"
        aria-label="menu"
        aria-expanded="false"
        @click="isOpen = !isOpen"
        v-bind:class="{'is-active': isOpen}"
      >
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>
    <div class="navbar-menu" v-bind:class="{'is-active': isOpen}">
      <div class="navbar-end">
        <nuxt-link class="navbar-item" to="/">Home</nuxt-link>
        <nuxt-link class="navbar-item" to="/about">About</nuxt-link>
        <nuxt-link class="navbar-item" to="/projects">Projects</nuxt-link>
        <nuxt-link class="navbar-item" to="/blog">Blog</nuxt-link>
        <nuxt-link class="navbar-item" to="/contact">Contact</nuxt-link>
      </div>
    </div>
  </nav>
</template>
<script>
export default {
  data: function() {
    return {
      isOpen: false
    };
  }
};
</script>