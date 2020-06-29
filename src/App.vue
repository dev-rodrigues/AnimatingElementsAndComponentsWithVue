<template>
  <div id="app">
    <div class="jumbotron jumbotron-fluid">
      <div class="container">
        <h1 class="display-4">Animações</h1>
        <p>Treinando transições/animações de elementos/componentes com VueJS.</p>
      </div>
    </div>
    <div class="container">
      <button
        class="btn btn-primary mb-3"
        @click="mostrar = !mostrar">Alternar</button>
      <div
      class="alert alert-primary"
      v-if="mostrar">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      mostrar: true,
    }
  }
}
</script>
