<template>
  <div>
    <h1>Meu nome é: {{ name }}</h1>
  </div>
</template>

<script>
  export default {
    name: 'LifeCycle',
    data() {
      return {
        name: 'Ainda não sei'
      }
    },
    created() {
      setTimeout(() => {
        this.name = 'Leonardo'
      }, 1000)
      this.lifeCycle()
    },

    mounted() {
      this.name = 'João'
      this.lifeCycle()
    },
    

    methods: {
      lifeCycle() {
        console.log('Executou')
      }
    }
  }
</script>