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
        name: '',
        email: ''
      }
    },

    methods: {
      enviarFormulario() {
        const name = this.name;
        const email = this.email;

        console.log('Formulário Enviado!')
        console.log('O nome é: ' + name)
        console.log('O email é: ' + email)

        // AJAX
        // Inserir no banco os dados
      }
    }
  }
</script>