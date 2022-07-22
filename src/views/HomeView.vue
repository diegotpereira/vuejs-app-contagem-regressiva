<template>
  <SiteFundo />
  <ContadoraCartao />
</template>

<script>
import SiteFundo from '../components/Fundo.vue'
import ContadoraCartao from '../components/Contadora.vue'

export default ({
  name: 'HomeView',

  components: {
    SiteFundo,
    ContadoraCartao
  },
});
</script>
