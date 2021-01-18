<template>
  <div id="app">
    <Header />

    <ul class="lista-categorias">
      <Categoria titulo="Todos" @click="atualizarCategoria('Teste')" />
      <li @click="atualizarCategoria('Teste')">
        <img src="@/assets/briefcase-solid.png">
        <p>Profissional</p>
      </li>
      <li>
        <img src="@/assets/university-solid.png">
        <p>Reguladores</p>
      </li>
      <li>
        <img src="@/assets/tree-solid.png">
        <p>Sócio Ambiental</p>
      </li>
      <li>
        <img src="@/assets/gavel-solid.png">
        <p>Jurídico</p>
      </li>
      <li>
        <img src="@/assets/ban-solid.png">
        <p>Listas Restritivas</p>
      </li>
      <li> 
        <img src="@/assets/gem-solid.png">
        <p>Mídia / Internet</p>
      </li>
      <li><img src="@/assets/globe-americas-solid.png">
        <p>Bens e Imóveis</p>
      </li>
      <li>
        <img src="@/assets/male-solid.png">
        <p>Cadastro</p>
      </li>
      <li>
        <img src="@/assets/piggy-bank-solid.png">
        <p>Financeiro</p>
      </li>
    </ul>
    
    <div class="buscar"><p>Ordenar</p>
      
      <select class="campo-pesquisa" v-model="selected">
      <option disabled value="">Lançamento</option>
      <option>Profissional</option>
      <option>Reguladores</option>
      <option>Sócio Ambiental</option>
      </select>
      <br>
</div> 

    <div class="container-cartao">
      <Card titulo="Profissional" icone="briefcase" preco="R$ 29,99" />
      <Card titulo="Reguladores" icone="university" corpo="O aplicativo Balanço Patrimonial realiza a consulta de todos os balanços que são publicados nos Diários Oficiais de empresas S.A., de capital aberto e limitadas (LTDA) de grande porte" preco="R$ 29,99" />
      <Card titulo="Sócio Ambiental" icone="tree" corpo="O aplicativo Balanço Patrimonial realiza a consulta de todos os balanços que são publicados nos Diários Oficiais de empresas S.A., de capital aberto e limitadas (LTDA) de grande porte" preco="R$ 29,99" />
      <Card titulo="Jurídico" icone="gavel" corpo="O aplicativo Balanço Patrimonial realiza a consulta de todos os balanços que são publicados nos Diários Oficiais de empresas S.A., de capital aberto e limitadas (LTDA) de grande porte" preco="R$ 29,99" />
      <Card titulo="Listas Restritivas" icone="ban" corpo="O aplicativo Balanço Patrimonial realiza a consulta de todos os balanços que são publicados nos Diários Oficiais de empresas S.A., de capital aberto e limitadas (LTDA) de grande porte" preco="R$ 29,99" />
      <Card titulo="Mídia/Internet" icone="globe" corpo="O aplicativo Balanço Patrimonial realiza a consulta de todos os balanços que são publicados nos Diários Oficiais de empresas S.A., de capital aberto e limitadas (LTDA) de grande porte" preco="R$ 29,99" url="/profissional" />
      <Card titulo="Bens e Imóveis" icone="gem" corpo="O aplicativo Balanço Patrimonial realiza a consulta de todos os balanços que são publicados nos Diários Oficiais de empresas S.A., de capital aberto e limitadas (LTDA) de grande porte" preco="R$ 29,99" url="/profissional" />
      <Card titulo="Cadastro" icone="male" corpo="O aplicativo Balanço Patrimonial realiza a consulta de todos os balanços que são publicados nos Diários Oficiais de empresas S.A., de capital aberto e limitadas (LTDA) de grande porte" preco="R$ 29,99" url="/profissional" />
      <Card titulo="Financeiro" icone="piggy-bank" corpo="O aplicativo Balanço Patrimonial realiza a consulta de todos os balanços que são publicados nos Diários Oficiais de empresas S.A., de capital aberto e limitadas (LTDA) de grande porte" preco="R$ 29,99" url="/profissional" />
      <Card titulo="Financeiro" icone="piggy-bank" corpo="O aplicativo Balanço Patrimonial realiza a consulta de todos os balanços que são publicados nos Diários Oficiais de empresas S.A., de capital aberto e limitadas (LTDA) de grande porte" preco="R$ 29,99" url="/profissional" />
      <Card titulo="Sócio Ambiental" icone="tree" corpo="O aplicativo Balanço Patrimonial realiza a consulta de todos os balanços que são publicados nos Diários Oficiais de empresas S.A., de capital aberto e limitadas (LTDA) de grande porte" preco="R$ 29,99" url="/profissional" />
      <Card titulo="Jurídico" icone="gavel" corpo="O aplicativo Balanço Patrimonial realiza a consulta de todos os balanços que são publicados nos Diários Oficiais de empresas S.A., de capital aberto e limitadas (LTDA) de grande porte" preco="R$ 29,99" url="/profissional" />
    </div>
  </div>
</template>

<style lang="scss">
  @import "@/styles/base.scss";
</style>

<script>
import Header from './components/Header/Header.vue'
import Card from './components/Card/Card.vue'
import Categoria from './components/Categoria/Categoria.vue'

export default {
  name: 'App',
  components: {
    Header,
    Card,
    Categoria,
  },
  data: () => ({
    categoriaAtual: null,
  }),
  watch: {
    categoriaAtual: function(novaCategoria) {
      alert(novaCategoria);
    }
  },
  methods: {
    atualizarCategoria: (chave) => {
      console.log(chave)
    }
  }
}
</script>

