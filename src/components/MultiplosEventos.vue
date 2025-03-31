<script>
export default {
    name: "MultiplosEventos",
    data() {
        return {
            multiplos_eventos: ""
        }
    },
    methods: {
        primeiro(e) {
            this.multiplos_eventos = "Primeiro evento ativado!"
        },
        segundo(e) {
            setTimeout(() => {
                this.multiplos_eventos = "Segundo evento ativado!"
            }, 2000)
        }
    }
}
</script>

<template>
    <div>
        <button @click="primeiro($event), segundo($event)"  class="border rounded-lg p-2">Ativar Múltiplos Eventos</button>
        <p>{{ multiplos_eventos }}</p>
    </div>
</template>