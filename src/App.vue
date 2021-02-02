<template>
  <div id="app">
    <!-- As a heading -->
    <b-container fluid class="header-nav">
      <b-navbar sticky toggleable="md" type="light">
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
          <b-navbar-nav>
            <b-nav-item to="/works">Nos Réalisations</b-nav-item>
            <b-nav-item to="/contact">Contact</b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </b-container>

    <router-view />
  </div>
</template>

<style lang="scss">
body {
  background-color: #fcfcfc;
}
#app {
  .header-nav{
    background-color: #fcfcfcf6;
    position: sticky!important;
    top: 0px;
    z-index: 100000;
    
  }
  img {
    max-width: 120px;
  }
  #nav-text-collapse {
    a {
      margin-right: 10px;
    }
  }
  .navbar-light .navbar-nav .nav-link {
    color: #111;
    font-weight: 600;
    letter-spacing: 1px;
    border-bottom: 0 solid #285b84;
    transition: border-bottom 100ms ease-in-out,
      padding-bottom 100ms ease-in-out;
    &:hover {
      padding-bottom: 0.1rem;
      border-bottom: 0.1rem solid #285b84;
    }
    & > :first-child {
      margin-top: 0;
    }
    & > :last-child {
      margin-top: 0;
    }
  }

  .sticky-top {
    padding-bottom: 50px;
    padding-top: 50px;
    width: 70%;
    margin: auto;
    border-bottom: 1px solid #285b847c;
     @media only screen and (max-width: 720px) {
      width: 100%;
    }
  }
@media only screen and (max-width: 720px) {
       .navbar-nav {
    display: flex;
    flex-direction: column;
    padding-left: 0;
    text-align: center;
    margin-top: 50px;
    margin-bottom: 0;
    list-style: none;
}
    }
 
}
</style>
