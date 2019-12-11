<template>
<div>
  <p>Paginas {{produtosPorPagina}} {{produtosTotal}}</p>
  <ul>
      <li><router-link :to="{query: {_page: 1}}">1</router-link></li>
  </ul>
</div>
</template>

<script>

export default {
    props: {
        produtosPorPagina: {
            type: Number,
            default: 1,
        },
        produtosTotal: {
            type: Number,
            default: 1, 
        }
    }
}
  
</script>

<style scoped>

</style>
