<template>
  <div>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">Projetos</a></li>
      <li><a href="#">Contato</a></li>
      <li v-if="logged"><a href="#">Meu Perfil</a></li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'CompHeader',
    props: ['logged']
  }
</script>

<!-- Scoped é algo parecido com !important -->
<style scoped>
  ul {
    background-color: #ccc;
    list-style: none;
    display: flex;
  }

  li {
    margin-right: 10px;
  }

  a {
    color: #000;
    text-decoration: none;
    transition: .5s;
  }

  a:hover {
    color: blue;
  }

</style>