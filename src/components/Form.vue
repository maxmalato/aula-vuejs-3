<script>
// import InputText from "./form/InputText.vue"
import Submit from "./form/Submit.vue"

export default {
    name: "Form",
    components: {
        // InputText,
        Submit
    },
    data() {
        return {
            name: "",
            email: ""
        }
    },
    methods: {
        sendForm(e) {
            e.preventDefault()

            const name = this.name
            const email = this.email

            alert(`Olá ${name}! Seu e-mail é ${email}`)

            // Depois disso será informado os dados ao banco de dados.
        }
    }
}
</script>

<template>
    <div>
        <form action="" class="flex flex-col gap-2" @submit="sendForm($event)">
            <div class="flex flex-col gap-3">
                <input type="text" v-model="name" class="border">
                <input type="text" v-model="email" class="border">
            </div>
            <Submit />
        </form>
    </div>
</template>