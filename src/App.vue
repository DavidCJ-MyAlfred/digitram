<template>
  <v-app>
    
    
    <AppBar/>

    <v-content>
      <ParticlesJS/>
      
    </v-content>
  <Footer/>
  </v-app>
</template>

<script>
import Footer from './components/Footer';
import ParticlesJS from './components/ParticlesJS';
import AppBar from './components/AppBar';


export default {
  name: 'App',

  components: {

    Footer,
    ParticlesJS,
    AppBar,
  },

  data: () => ({
    //
  }),
};
</script>
