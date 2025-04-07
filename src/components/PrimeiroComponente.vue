<template>
  <div>
    <h1 class="text-green-700 font-semibold">Olá, VueJS!</h1>
    <p>Nome: {{ nome }}</p>
    <p>profissao: {{ profissao }}</p>
    <MultiplosEventos />
    <Reutilizacao />
    <Reutilizacao />
    <Reutilizacao />
    <Reutilizacao />
    <Reutilizacao />
    <Reutilizacao />
    <Reutilizacao />
    <Reutilizacao />
  </div>
</template>

<script>
import MultiplosEventos from "./MultiplosEventos.vue"
import Reutilizacao from "./Reutilizacao.vue"

export default {
  name: "PrimeiroComponente",
  components: {
    MultiplosEventos,
    Reutilizacao
  },
  data() {
    return {
      nome: "Maxjannyfer Malato",
      profissao: "Desenvolvedor Frontend"
    }
  }
};
</script>