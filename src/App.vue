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
        <transition name="fade">
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
  .fade-enter {
    opacity:0;
  }

  .fade-enter-active {
    transition: opacity 1s;
  }

  .fade-enter-to {
    opacity:1;
  }

  /*SAIDA*/
    .fade-leave {
      opacity:1;
  }

  .fade-leave-active {
    transition: opacity 1s;
  }

  .fade-leave-to {
    opacity:0;
  }
</style>
