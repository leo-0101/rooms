<template>
  <div>
    <button @click="first('PRIMEIRO EVENTO!'), sec('SEGUNDO EVENTO!'), trd()">Ativar múltiplos eventos</button>
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
      first(txt) {
        this.multiplosEventos = txt;
      },
      sec(txt) {
        setTimeout(() => this.multiplosEventos = txt, 500)
      },

      trd() {
        setTimeout(() => this.multiplosEventos = "", 1000)
      }
    }
  }
</script>

<style scoped>
  div {
    margin: 100px;
  }
</style>
