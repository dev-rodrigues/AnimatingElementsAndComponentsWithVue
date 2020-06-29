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
        <transition>
          <div
            class="alert alert-primary"
            v-if="mostrar">
          </div>  
        </transition>      
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

<style scope>

  /*ENTRADA*/
  .v-enter {
    opacity:0;
  }

  .v-enter-active {
    transition: opacity 1s;
  }

  .v-enter-to {
    opacity:1;
  }

  /*SAIDA*/
    .v-leave {
      opacity:1;
  }

  .v-leave-active {
    transition: opacity 1s;
  }

  .v-leave-to {
    opacity:0;
  }
</style>
