<template>
  <Navbar />
  
  <router-view/>
  
  <medios-pago/>
  <Footer />
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import Footer from '@/components/Footer.vue'
import MediosPago from '@/components/MediosPago.vue'
import router from './router';

export default {
  name: 'HomeView',
  components: {
    Navbar,
    Footer,
    MediosPago
  },
 
}
</script>
