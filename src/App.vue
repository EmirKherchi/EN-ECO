<template>
  <div id="app">
    <!-- As a heading -->
    <b-navbar sticky toggleable="sm" variant="faded" type="light">
      <b-navbar-toggle target="nav-text-collapse"></b-navbar-toggle>
      <b-navbar-brand  tag="h1" to="/" class="mb-0">
        <b-img
        fluid
          src="./assets/images/Original.svg"
          class="d-inline-block align-top"
          alt="Logo entreprise isolation 1euro en eco normandie"
        />
      </b-navbar-brand>
      <b-collapse id="nav-text-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item to="/about">About</b-nav-item>
          <b-nav-item to="/contact">contact</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>

   
    <router-view />
  </div>
</template>

<style lang="scss">
#app {
  img {
   max-width: 100px;
  }
 #nav-text-collapse{
  margin-left: 35%;
    a{
  margin-right: 100px;
}
  }

}
</style>
