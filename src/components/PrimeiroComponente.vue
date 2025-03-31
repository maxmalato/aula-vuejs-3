<template>
  <div>
    <h1 class="text-green-700 font-semibold">Olá, VueJS!</h1>
    <p>Nome: {{ nome }}</p>
    <p>profissao: {{ profissao }}</p>
    <MultiplosEventos />
  </div>
</template>

<script>
import MultiplosEventos from "./MultiplosEventos.vue"

export default {
  name: "PrimeiroComponente",
  components: {
    MultiplosEventos
  },
  data() {
    return {
      nome: "Maxjannyfer Malato",
      profissao: "Desenvolvedor Frontend"
    }
  }
};
</script>