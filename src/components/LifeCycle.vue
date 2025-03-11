<template>
    <h1 class="text-xl">Meu nome é: {{ nome }}</h1>
</template>

<script>
    export default {
        name: "LifeCycle",
        data() {
            return {
                nome: "Ainda não sei"
            }
        },
        // Assim que a página foi carregada, o nome do dado foi alterado.
        created() {
            setTimeout(() => {
                this.nome = "Max Malato"
            }, 2000)

            this.lifeCycle()
        },
        // Depois que é criado, será montado.
        mounted() {
            setTimeout(() => {
                this.nome = "Ana Caroline"
            }, 2000)
        },
        methods: {
            lifeCycle() {
                console.log("Executou.")
            }
        }
    }
</script>