<script>
export default {
  data() {
    return {
      destino: "",
    };
  },
  methods: {
    go() {
      this.$router.push(this.destino);
    },
  },
};
</script>

<template>
  <header>
    <div class="cabecalho">
      <div>
        <span class="cabecalho-span">
          <RouterLink to="/">FilmeShow</RouterLink>
        </span>
        <span>
          <select v-model="destino" @change="go" class="select-cabecalho">
            <option value="" disabled>Categorias</option>
            <option value="/acao">açao e aventura</option>
            <option value="/terror">Terror</option>
            <option value="/animacao">Animaçao</option>
            <option value="/ficcao">Ficcao Cientifica</option>
            <option value="/suspense">Suspense</option>
            <option value="/fantasia">Fantasia</option>
            <option value="/comedia">Comedia</option>
            <option value="/drama">Drama</option>
            <option value="/romance">Romance</option>
          </select>
        </span>
        <span class="cabecalho-span"
          ><RouterLink to="/lancamento">Lançamentos</RouterLink></span
        >
      </div>
      <div>
        <span class="cabecalho-span">Minha Conta</span>
        <button>
          <RouterLink to="/pesquisa" class="button-pesquisar"
            >Pesquisar
          </RouterLink>
        </button>
      </div>
    </div>
  </header>
</template>
