<script>

export default {
    name: "Reutilizacao",
    data() {
        return {
            ativou: false
        }
    },
    methods: {
        ativar() {
            this.ativou = !this.ativou
        }
    }
}
</script>

<template>
    <div>
        <h1>Reutilização de Componentes</h1>

        <button @click="ativar" class="bg-blue-500 text-white p-2 rounded-md">Clique aqui!</button>
        <span v-show="ativou" class="text-green-500">Ativado!</span>
    </div>
</template>