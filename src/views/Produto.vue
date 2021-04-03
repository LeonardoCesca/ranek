<template>
  <p>Produto {{id}}</p>
</template>

<script>
export default {
  name: "produto",
  props: ["id"]
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
