<template>
  <div id="app">
    <!-- As a heading -->
    <b-navbar sticky toggleable="md" variant="faded" type="light">
      <b-navbar-toggle target="nav-text-collapse"></b-navbar-toggle>
      <b-navbar variant="faded" type="light">
        <b-navbar-brand to="/">
          <b-img
            fluid
            src="./assets/images/logo.png"
            class="d-inline-block align-top"
            alt="Logo entreprise isolation 1euro en eco normandie"
          />
        </b-navbar-brand>
      </b-navbar>

      <b-collapse id="nav-text-collapse" class="justify-content-end" is-nav>
        <b-navbar-nav >
          <b-nav-item to="/works">Nos Réalisations</b-nav-item>
          <b-nav-item to="/contact">Contact</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>

    

    <router-view />
  </div>

  
</template>

<style lang="scss">
#app {
  body {
    background-color: #fcfcfc;
  }
  img {
    max-width: 120px;
  }
  #nav-text-collapse {
    //margin-left: 40%;
    a {
      margin-right: 10px;
    }
  }
  .navbar-light .navbar-nav .nav-link {
    color: #111;
    font-weight: 500;
  }
  .sticky-top {
    padding-bottom: 50px;
    padding-top: 50px;
    width: 70%;
    margin: auto;
    border-bottom: 1px solid #285b847c;
  }
}
</style>
