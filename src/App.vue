<script>
import LifeCycle from './components/LifeCycle.vue'
import Pessoa from './components/Pessoa.vue'

export default {
  name: "App",
  components: {
    LifeCycle,
    Pessoa
  }
}
</script>

<template>
  <LifeCycle />
  <Pessoa />
</template>
