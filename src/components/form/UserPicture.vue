<template>
  <!-- : mesmo que v-bind -->
  <img :src="avatar" :alt="descr">  
</template>

<script>
export default {
  name: 'UserPicture',
  data() {
    return {
      // a barra acessa diretamente o public
      avatar: '/img/avatar.png',
      descr: 'Leonardo Oliveira'
    }
  }
}
</script>