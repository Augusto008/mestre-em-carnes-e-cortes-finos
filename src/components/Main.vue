<template>
  <div class="hello">
    <h1 class="pb-5">{{ msg }}</h1>
    <h3 class="pt-5">
      Bem vindo ao curso de carnes e cortes!
    </h3>
    <p>
      Aqui você vai aprender tudo o que precisa para trabalhar neste ramo.<br />
    </p>
    <p>
      O material, aqui disposto, é dividido em duas partes:
    </p>
    <table class="table table-bordered my-5">
      <thead>
        <tr>
          <th width="50%"><router-link to="/trilha">Trilha</router-link></th>
          <th width="50%"><router-link to="/pratica">Prática</router-link></th>
        </tr>
      </thead>
      <tbody class="table-group-divider">
        <tr>
          <td>Objetiva apresentar a teoria, introduzindo os conceitos necessários para que possas alcançar os melhores resultados práticos.</td>
          <td>Contém todos os exercícios para avaliação e teste de conhecimento.</td>
        </tr>
      </tbody>
    </table>
    <p>
      Você vai perceber, no decorrer do curso que o conteúdo não estará totalmente disponível de imediato.<br>
      Todos iniciarão da mesma maneira, independente do tempo de experiência que possuem e poderão acessar os níveis mais avançados à medida em que passarem nos testes propostos para cada um.<br>
    </p>
    <p class="border rounded mt-5">
      <strong>Aviso</strong>:<br>
      Para passar de nível será exigido o resultado de uma próva prática que deverá ser aplicada pelo supervisor do setor.<br>
      Caso haja a possibilidade de uma promoção, o supervisor aplicará a prova no candidato e, se este passar, poderá exercer a função.
    </p>
    <div class="py-5"></div>
    <p class="text-justify">
      Este curso é gratuito e tem o intuito de incentivar a busca pelo conhecimento, diminuir as dúvidas e evitar acidentes.<br>
      Procure estudar e praticar o que aprender aqui.<br>
      Busque melhorar sempre e preste muita atenção às normas de segurança para evitar acidentes, resguardando, assim, a sua vida e a dos demais integrantes da equipe.
    </p>
    <div class="my-5 py-5"></div>
    <p>Para mais informações, procure seu supervisor.</p>
  </div>
  <h3 class="pt-5">

  </h3>
</template>

<script>
export default {
  name: 'Main',
  props: {
    msg: String
  }
}
</script>

<style lang="scss">
  .table {
    th, td {
      background-color: transparent;
      color: #FFFFFF;
    }
  }
</style>
