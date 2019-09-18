<template>
  <div class="jumbotron jumbotron-fluid">
    <div class="container">
      <h1 class="display-3">Loja online</h1>
      <p class="lead">Mais informaçoes</p>
      <hr class="my-2" />
      <p>Detalhes</p>
      <p class="lead">
        <a class="btn btn-primary btn-lg" href="#" role="button">Detalhes</a>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Jumbotron",
  props: {
    product: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
a {
  color: #42b983;
}
</style>
