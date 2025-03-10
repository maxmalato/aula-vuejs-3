<script>
import Info from "./Info.vue"
import Form from "./Form.vue";

export default {
    name: "Pessoa",
    data() {
        return {
            nome: "Max"
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
        <Info/>
        <Form/>
    </div>
</template>
