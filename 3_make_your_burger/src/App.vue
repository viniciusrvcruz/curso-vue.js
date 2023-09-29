<template>
  <NavbarContent :logo="logo_src" :alt="app_name"/>
  <RouterView />
  <Footer />
</template>

<script>
import NavbarContent from './components/Navbar.vue';
import Footer from './components/Footer.vue';

  export default {
    name: 'Navbar',
    components: {
      NavbarContent,
      Footer
    },
    data() {
      return {
        logo_src: '/img/logo.png',
        app_name: 'Make Your Burger '
      }
    }
  }
</script>

<style>
  * {
    font-family: Helvetica, sans-serif;
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }

  .main-container {
    margin: 50px;
    min-height: 420px;
  }

  h1 {
    text-align: center;
    font-size: 42px;
    margin-bottom: 30px;
    color: #222;
  }
</style>