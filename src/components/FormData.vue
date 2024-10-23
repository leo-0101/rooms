<template>
  <div>
    <h2>Meu formulário:</h2>
    <!-- prevent == prevent.default() -->
    <form action="" @submit.prevent="enviarFormulario">
      <div>
        <input type="text" v-model='name'>
      </div>
      
      <div>
        <input type="text" v-model='email'>
      </div>

      <div>
        <InputSubmit/>
      </div>
    </form>    
  </div>
</template>

<script>
// import InputText from './form/InputText.vue'
import InputSubmit from './form/InputSubmit.vue'


  export default {
    name: 'FormData',
    components: {
      // InputText,
      InputSubmit
    },

    data() {
      return {
        name: 'Leonardo',
        email: 'leo@email.com'
      }
    },

    methods: {
      enviarFormulario() {
        console.log('Formulário Enviado!')
      }
    }
  }
</script>