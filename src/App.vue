<template>
  <nav>
    <router-link to="/">Início</router-link> |
    <router-link to="/trilha">Trilha</router-link> |
    <router-link to="/pratica">Prática</router-link> |
    <router-link to="/referencias">Referências</router-link>
  </nav>
  <div id="content" class="col-10 mx-auto">
    <router-view/>
  </div>
  <img class="img-fluid" src="@/assets/backgrounds/fire-bottom-removebg-preview.png" width="100%">
</template>

<script>
  //import Swal from 'sweetalert2';

  //export default {
  //  methods: {
  //    welcome() {
  //      Swal.fire('Bem vindo!');
  //    }
  //  },
  //  mounted() {
  //    this.welcome();
  //  }
  //}

</script>

<style lang="scss">
//Vermelho e preto: #FF0000 e #000000
//Azul e laranja: #0000FF e #FFA500
//Branco e cinza: #FFFFFF e #808080
//Marrom e amarelo: #A52A2A e #FFFF00

body {
  background-image: url('assets/backgrounds/bg-cuts.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  margin: 0;
  padding: 0;
}

#app {
  min-height: 100vh;
  background-color: #00000080;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #FFFFFF;

  h1 {
    text-shadow: 
      0 0 2px #FFC04C72,
      0 0 2px #FFC04C72,
      0 0 2px #FF0000,
      0 0 4px #FFC04C72,
      0 0 4px #FFC04C72,
      0 0 6px #FFC04C72,
      0 0 6px #FFC04C72,
      0 0 8px #FFC04C72,
      0 0 8px #FFC04C72;
    color: #FFFF6E;
  }
  
  h2, h3 {
    margin: 40px 0 0;
  }
  
  ul {
    list-style-type: none;
    padding: 0;
  }
  
  li {
    display: inline-block;
    margin: 0 10px;
  }
  
  a {
    color: #FFA500;
  }
  
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #FF0000;

    &.router-link-exact-active {
      text-shadow: 
        0 0 2px #C0C0C072,
        0 0 2px #C0C0C072,
        0 0 4px #C0C0C072,
        0 0 4px #C0C0C072;
      color: #FFFF6E;
    }

    &:hover {
      text-shadow: 
        0 0 2px #FFFF6E72,
        0 0 2px #FFFF6E72,
        0 0 4px #FFFF6E72,
        0 0 4px #FFFF6E72;
      color: #FAFAFA;
    }
  }
}

.text-justify {
  text-align: justify;
}
</style>
