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

    <b-container fluid class="footer">
      <b-navbar-nav class="footer-main mx-auto" style="max-width: 800px;">
        <ul class="topnav">
          <li>
            <b-img
              class="logoRge"
              src="./assets/images/logoRge.png"
              alt="Facebook entreprise isolation 1euro en eco normandie"
            />
            <br />
            <p class="logoRge_text">E-E 184 925</p>
          </li>

          <router-link tag="li" to="/mentions" class="footer-text_link"
            ><a>Mentions légales</a></router-link
          >
          <router-link tag="li" to="/contact" class="footer-text_link"
            ><a>Contact</a></router-link
          >
          <router-link tag="li" to="/mentions"
            ><a
              ><b-img
                src="./assets/images/Facebook_logo.png"
                alt="Facebook entreprise isolation 1euro en eco normandie"/></a
          ></router-link>
          <router-link tag="li" to="/mentions"
            ><a
              ><b-img
                src="./assets/images/Instagram_logo.png"
                alt="Instagram entreprise isolation 1euro en eco normandie"/></a
          ></router-link>
        </ul>
      </b-navbar-nav>
    </b-container>
  </div>
</template>

<style lang="scss">
body {
  background-color: #fcfcfc;
}
#app {
  .logoRge {
   display: block;
    margin: 10px auto;
    margin-bottom: 0;
    width: 32px;
    &_text {
      color: #fcfcfc;
      font-size: 10px;
      letter-spacing: 1px;
    }
  }
  .header-nav {
    background-color: #fcfcfcf6;
    position: sticky !important;
    top: 0px;
    z-index: 100000;
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
  .footer {
    background-color: #111;
    padding: 45px 0px;
    &-text_link {
      margin-top: 5px;
    }
    ul.topnav {
      list-style-type: none;
      margin: 0;
      padding: 0;
      overflow: hidden;
      display: block;
      margin: auto;
    }
    ul.topnav li {
      float: left;
    }
    ul.topnav li a {
      display: block;
      color: #fbfbfd;
      text-align: center;
      padding: 1rem;
      text-decoration: none;
      letter-spacing: 1px;
      &:hover {
        color: #5ea669;
        transition: all 500ms ease;
      }
    }

    @media screen and (max-width: 600px) {
      ul.topnav,
      ul.topnav li {
        float: none;
      }
    }
  }
}
</style>
