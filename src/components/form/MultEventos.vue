<template>
  <div>
    <button @click="first(), sec()">Ativar múltiplos eventos</button>
    <p>{{ multiplosEventos }}</p>
  </div>
</template>

<script>
  export default {
    name: 'MultEventos',
    data() {
      return {
        multiplosEventos: ''
      };
    },

    methods: {
      first() {
        this.multiplosEventos = 'Primeiro evento ativado!';
      },
      sec() {
        setTimeout(() => this.multiplosEventos = 'Segundo evento!', 500)
      }
    }
  }
</script>

<style scoped>
  div {
    margin: 100px;
  }
</style>
