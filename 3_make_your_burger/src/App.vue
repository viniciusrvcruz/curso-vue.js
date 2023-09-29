<template>
  <NavbarContent />
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
    }
  }
</script>

<style scoped>

</style>