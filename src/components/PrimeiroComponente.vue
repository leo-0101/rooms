<template>
  <div>
    <h1>Olá Vue!</h1>
    <p>Meu nome é {{ name }} e trabalho como {{ job }}</p>
    <MultEventos/>
  </div>
  
</template>

<script>
  import MultEventos from './form/MultEventos.vue'

  export default {
    name: 'PrimeiroComponente',
    components: {
      MultEventos
    },

    data() {
      return {
        name: 'Leonardo',
        job: 'Programador'
      }
    }
  }
</script>