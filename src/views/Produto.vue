<template>
  <p>Produto {{id}}</p>
</template>

<script>
import {api} from '@/services/services.js';
export default {
  name: "produto",
  props: ["id"],
  data() {
    return {
      produto: null,
    }
  },
  methods: {
    getProduto() {
      api.get(`/produto/${this.id}`)
        .then(response => {
          this.produto = response.data;
        })
    },
    created() {
      this.getProduto();
    }
  }
};
</script>

<style scoped>
  p {
    color: #87f;
    margin-top: 40px;
    font-size: 2rem;
    text-align: center;
  }
</style>
