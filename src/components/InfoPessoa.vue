<template>
  <div>
    <p v-if="working">Estou trabalhando no momento.</p>
    <p v-else>Estou passando fome</p>

    <p>Utilizo as seguintes tecnologias para backend:</p>
    <ul>
      <li v-for="(technology, index) in be_tech" :key="index">{{ technology }}</li>
    </ul>

    <p>Utilizo as seguintes tecnologias para frontend:</p>
    <ul>
      <li v-for="technology in fe_tech" :key="technology.id">{{ technology.language }}</li>
    </ul>

    <div>
      <button @click="showEmail">{{ textoBotao }}</button>
    </div>

    <p v-show="show_email">Mande uma mensagem para: {{ email }}</p>
    <p>Para acessar meu portfólio basta clicar <a v-bind:href="meu_link" target="_blank">aqui</a></p>

    <UserPicture/>
  </div>
</template>

<script>
  import UserPicture from './form/UserPicture.vue';

  export default {
    name: 'InfoPessoa',
    components: {
      UserPicture
    },

    data() {
      return {
        working: true,
        show_email: false,
        email: 'leonardo@email.com',
        meu_link: 'https://google.com',
        textoBotao: 'Mostrar e-mail',

        be_tech: ['PHP', 'JavaScript', 'Kotlin'],
        // fe_tech: ['Vue', 'Angular', 'React']
        fe_tech: [
          {id: 1, language: 'Vue'},
          {id: 2, language: 'Angular'},
          {id: 3, language: 'Kotlin'}
        ]
      }
    },
    methods: {
      showEmail() {
        // faz o inverso do que está
        this.show_email = !this.show_email

        if(!this.show_email) {
          this.textoBotao = 'Mostrar e-mail'
        } else {
          this.textoBotao = 'Esconder e-mail'
        }
      }
    }
  }
</script>