<template>
  <div>
    <h2>Descrição da pessoa: {{ nome }} </h2>
    <InfoPessoa :email="email" :working=true />
    <FormData/>
  </div>
</template>

<script>
  import InfoPessoa from './InfoPessoa'
  import FormData from './FormData'

  export default {
    name: 'DadosPessoa',
    components: {
      InfoPessoa,
      FormData
    },

    data() {
      return {
        nome: 'Leonardo',
        email: 'julliakristina2@email.com'
      }
    }
  }
</script>