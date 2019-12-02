<template>
  <div>
    <!-- navigation -->
    <nav class="navbar is-white" role="navigation" aria-label="main navigation">
      <div class="container">
        <div class="navbar-start">
          <nuxt-link to="/" class="navbar-item">Awesome JS SSR Blog!</nuxt-link>
          <nuxt-link active-class="is-active" to="/" class="navbar-item is-tab" exact>Home</nuxt-link>
          <nuxt-link active-class="is-active" to="/about" class="navbar-item is-tab" exact>About</nuxt-link>
        </div>
      </div>
    </nav>
    <!-- /navigation -->
    <nuxt />
  </div>
</template>

<style>
.main-content {
  margin: 30px 0;
}
</style>
