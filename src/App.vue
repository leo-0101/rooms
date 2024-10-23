<template>
  <CompHeader/>
  <PrimeiroComponente/>
  <LifeCycle/>
  <DadosPessoa/>
</template>

<script>
  import CompHeader from './components/CompHeader.vue'
  import PrimeiroComponente from './components/PrimeiroComponente.vue'
  import LifeCycle from './components/LifeCycle.vue'
  import DadosPessoa from './components/DadosPessoa.vue'

  export default {
    name: 'App',
    components: {
      CompHeader,
      PrimeiroComponente,
      LifeCycle,
      DadosPessoa
    }
  }
</script>

<style>
  body {
    background-color: #000;
    color: #fff;
  }

  a {
    color: red;
  }
</style>