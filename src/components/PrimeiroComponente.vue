<template>
  <div>
    <h1 class="text-green-700 font-semibold">Olá, VueJS!</h1>
    <p>Nome: {{ nome }}</p>
    <p>profissao: {{ profissao }}</p>
  </div>
</template>

<script>
export default {
  name: "PrimeiroComponente",
  data() {
    return {
      nome: "Maxjannyfer Malato",
      profissao: "Desenvolvedor Frontend"
    }
  }
};
</script>