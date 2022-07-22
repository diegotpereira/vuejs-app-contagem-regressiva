<template>
  <SiteFundo>
    <EmBreve />
     <ContadoraCartao />
     <InscrevaSe />
     <FooterBg />
  </SiteFundo>
  
</template>

<script>
import EmBreve from '../components/EmBreve.vue'
import SiteFundo from '../components/Fundo.vue'
import ContadoraCartao from '../components/Contadora.vue'
import InscrevaSe from '../components/InscrevaSe.vue'
import FooterBg from '../components/Footer.vue'

export default ({
  name: 'HomeView',

  components: {
    EmBreve,
    SiteFundo,
    ContadoraCartao,
    InscrevaSe,
    FooterBg
  },
});
</script>
