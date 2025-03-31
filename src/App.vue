<script>
import LifeCycle from './components/LifeCycle.vue'
import Pessoa from './components/Pessoa.vue'
import PrimeiroComponente from './components/PrimeiroComponente.vue'

export default {
  name: "App",
  components: {
    LifeCycle,
    Pessoa,
    PrimeiroComponente
  }
}
</script>

<template>
  <PrimeiroComponente/>
  <LifeCycle />
  <Pessoa />
</template>
