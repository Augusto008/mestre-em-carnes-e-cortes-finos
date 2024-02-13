<template>
  <div class="lesson">
    <h1 class="py-5">Normalização e Segurança</h1>
    <p class="mb-5 pb-5">
      Em um ramo como este onde ferramentas de corte são utilizadas com tanta frequência, estamos sujeitos a acidentes à todo momento.<br>
      Pensando nisso, é muito importante que, antes de aprender sobre quaisquer ferramentas descritas neste curso, você entenda os perigos que cada uma oferece para você e para os membros da sua equipe.<br>
      Uma vez absorvidas as informações dessa lissão, você será um profissional mais conciente e, ao aplicar isso no seu trabalho, mais competente.
    </p>
    <h3>
      Normas Regulamentadoras - NR
    </h3>
    <p class="mb-5 text-justify">
      Segundo o site 
      <a href="https://www.gov.br/trabalho-e-emprego/pt-br/assuntos/inspecao-do-trabalho/seguranca-e-saude-no-trabalho/ctpp-nrs/normas-regulamentadoras-nrs" target="_blank">gov.com.br</a>:
      As normas regulamentadoras (NR)
      <q cite="https://www.gov.br/trabalho-e-emprego/pt-br/assuntos/inspecao-do-trabalho/seguranca-e-saude-no-trabalho/ctpp-nrs/normas-regulamentadoras-nrs">consistem em obrigações, direitos e deveres a serem cumpridos por empregadores e trabalhadores com o objetivo de garantir trabalho seguro e sadio, prevenindo a ocorrência de doenças e acidentes de trabalho.</q>
    </p>
    <h3>NR 36 - SEGURANÇA E SAÚDE NO TRABALHO EM EMPRESAS DE ABATE E PROCESSAMENTO DE CARNES E DERIVADOS</h3>
    <p>
      O objetivo desta Norma é estabelecer os requisitos mínimos para a avaliação, controle e monitoramento dos riscos existentes nas atividades desenvolvidas na indústria de abate e processamento de carnes e derivados destinados ao consumo humano, de forma a garantir permanentemente a segurança, a saúde e a qualidade de vida no trabalho, sem prejuízo da observância do disposto nas demais Normas Regulamentadoras - NR do Ministério do Trabalho e Emprego.
    </p>
    
    <div class="accordion rounded mb-5 pb-5" id="nr-list">
      <h4 class="accordion-header py-3">
        Dentre as Normas Regulamentadoras que regem nosso mercado estão:
      </h4>
      <div id="norms-list">
        <div class="accordion-item" v-for="(item, index) in lessonItems" v-bind:key="index">
          <button
            class="accordion-button collapsed"
            type="button"
            data-bs-toggle="collapse"
            :data-bs-target="`#` + item[1]"
            aria-expanded="false"
            :aria-controls="`#` + item[1]"
          >
            {{ item[1] }} - {{ item[2] }}
          </button>
          <div
            :id="item[1]"
            class="accordion-collapse collapse"
            data-bs-parent="#nr-list"
          >
            <div class="accordion-body">
              <p v-html="item[3]"></p>
            </div>
          </div>
        </div>
      </div>
      <p class="pt-4 text-justify">
        No decorrer desta lissão nós vamos estudar um pouco mais profundamente cada uma destas normas no que diz respeito à nossa atuação, principalmente a NR-36. Vamos ver algumas situações para entender a importância de certas precauções e os riscos e perigos aos quais estamos expostos.
      </p>
      <p>
        Leia atentamente às informações e realize as atividades propostas para desbloquear a próxima NR.<br>
        Assim que tiveres realizado as atividades das 4 NRs, a prórima lissão será liberada.
      </p>
    </div>
    <div id="tests">
      <nav class="row justify-content-center" id="navTest">
        <div class="col-auto my-2" v-for="(item, index) in lessonItems" v-bind:key="index" :value="item[0]">
          <button class="btn btn-light" @click="changeComponent(item[0])">
            {{ item[1] }}
          </button>
        </div>
      </nav>
      <component v-bind:is="selectedLessonItem"></component>
    </div>
  </div>
</template>

<style lang="scss">
  .accordion {

    div, button {
      color: #FFFFFF !important;
      background-color: transparent !important;
    } 

    .accordion-collapse {
      background-color: #00000032 !important;
    }

    .accordion-item {

      .accordion-button {
        backdrop-filter: blur(8px);
      }

      .accordion-button:focus {
        background-image: linear-gradient(#00000064, #00000064);
      }
      
      .show {
        backdrop-filter: none;
      }

    }

    #norms-list {
      text-align: justify;
      background-image: url('@/assets/backgrounds/bg-burnt-wood.avif') !important;
      background-size: cover;
      background-position: center;
    }

  }
</style>

<script>
  import NR12 from './tests/NR12.vue'
  import NR17 from './tests/NR17.vue'
  import NR24 from './tests/NR24.vue'
  import NR36 from './tests/NR36.vue'

  export default {
    name: "Lesson1",
    components: {
      NR12,
      NR17,
      NR24,
      NR36,
    },
    data() {
      return {
        lessonItems: [
          ['NR12', 'NR-12', 'SEGURANÇA NO TRABALHO EM MÁQUINAS E EQUIPAMENTOS', 'Contém informações importantes sobre como agir em atividades que envolvam o uso de Máquinas e Equipamentos.<br>Embora abranja muitas máquinas que não estão relacionadas a carnes, também contém regras específicas para a utilização de máquinas e equipamentos como serras fita  que são utilizadas em açougue, por exemplo.'],
          ['NR17', 'NR-17', 'ERGONOMIA', 'Trata da ergonomia no ambiente de trabalho e pode ser aplicada para atividades que envolvam o manuseio de carnes.<br>Aponta informações importantes para nos manter saudáveis e evitar problemas de postura, dores no corpo e até problemas psicológicos como stress, por exemplo.'],
          ['NR24', 'NR-24', 'CONDIÇÕES SANITÁRIAS E DE CONFORTO NOS LOCAIS DE TRABALHO', 'Estabelece requisitos para garantir condições adequadas de higiêne para evitar possíveis contaminações ao produto e ao cliente.'],
          ['NR36', 'NR-36', 'SEGURANÇA E SAÚDE NO TRABALHO EM EMPRESAS DE ABATE E PROCESSAMENTO DE CARNES E DERIVADOS', 'Específica para trabalhos que envolvem manipulação de carnes, é a mais importante para o nosso ramo.<br>Esta norma aborda uma série de requisitos para garantir a segurança e saúde dos trabalhadores do setor.'],
        ],
        selectedLessonItem: "NR12",
      }
    },
    computed: {
      actualComponent() {
        return this.selectedLessonItem;
      }
    },
    methods: {
      changeComponent(target) {
        return this.selectedLessonItem = target;
      }
    }
  }
</script>