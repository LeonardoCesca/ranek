<template>
  <div>
    <p>Paginas {{ paginasTotal }}</p>
    <ul>
      <li v-for="pagina in paginasTotal" :key="pagina">
        <router-link :to="{ query: { _page: pagina } }">
          {{ pagina }}
        </router-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    produtosPagina: {
      type: Number,
      default: 1
    },
    produtosTotal: {
      type: Number,
      default: 1
    }
  },
  computed: {
    paginasTotal() {
      const total = this.produtosTotal / this.produtosPagina;
      return total !== Infinity ? Math.ceil(total) : 0;
    }
  }
};
</script>

<style scoped></style>
