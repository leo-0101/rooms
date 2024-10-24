<template>
  <div>
    <ReutComp/>
    <h1>Olá Vue!</h1>
    <ReutComp/>
    <p>Meu nome é {{ name }} e trabalho como {{ job }}</p>
    <ReutComp/>
    <MultEventos/>
    <ReutComp/>
  </div>
  
</template>

<script>
  import MultEventos from './form/MultEventos.vue'
  import ReutComp from './ReutComp.vue'

  export default {
    name: 'PrimeiroComponente',
    components: {
      MultEventos,
      ReutComp
    },

    data() {
      return {
        name: 'Leonardo',
        job: 'Programador'
      }
    }
  }
</script>