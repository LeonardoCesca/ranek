<template>
  <div>
    <p>Paginas {{ paginasTotal }}</p>
    <ul>
      <li><router-link :to="{ query: { _page: 1 } }">1</router-link></li>
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
      return Math.ceil(total);
    }
  }
};
</script>

<style scoped></style>
