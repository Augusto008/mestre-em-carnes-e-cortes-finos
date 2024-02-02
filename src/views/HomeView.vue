<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/knife-cut.svg" class="my-5 pb-5" style="width: 50%; max-width: 500px; min-width: 200px;">
    <Main msg="Mestre em Carnes e Cortes Finos"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Main from '@/components/Main.vue'

export default {
  name: 'HomeView',
  components: {
    Main
  }
}
</script>
