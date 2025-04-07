<script>
import Info from "./Info.vue"
import Form from "./Form.vue";

export default {
    name: "Pessoa",
    data() {
        return {
            nome: "Max",
            email: "max@gmail.com",
            isWorking: false
        }
    },
    methods: {
        trabalhando() {
            this.isWorking = !this.isWorking
        }
    },
    components: {
        Info,
        Form
    }
}
</script>

<template>
    <div>
        <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
        <Info :compEmail="email" :isWorking="isWorking"/>   
        <Form/>
        <button class="bg-blue-500 text-white p-2 rounded-md" @click="trabalhando">Trabalhando</button>
    </div>
</template>
