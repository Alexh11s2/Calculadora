<template>
  <div class="container py-5" style="max-width: 500px">
    <h1 class="h3 mb-4">Calculadora de Promedio</h1>

    <NotaInput etiqueta="Bloque 1 (20%)" v-model="bloque1" />
    <NotaInput etiqueta="Bloque 2 (20%)" v-model="bloque2" />
    <NotaInput etiqueta="Bloque 3 (20%)" v-model="bloque3" />
    <NotaInput etiqueta="Proyecto final (40%)" v-model="proyecto" />

    <button class="btn btn-primary w-100" @click="mostrar = true"> Calcular promedio
    </button>
    <ResultadoFinal v-if="mostrar" :promedio="promedio" />
  </div>
</template>

<script>
import NotaInput from './components/NotaInput.vue'
import ResultadoFinal from './components/ResultadoFinal.vue'

export default {
  name: 'App',
  components: { NotaInput, ResultadoFinal },
  data() {
    return {
      bloque1: 0,
      bloque2: 0,
      bloque3: 0,
      proyecto: 0,
      mostrar: false
    }
  },
  computed: {
    promedio() {
      return this.bloque1 * 0.2 + this.bloque2 * 0.2 + this.bloque3 * 0.2 +
this.proyecto * 0.4
    }
  }
}
</script>

<style>

</style>
