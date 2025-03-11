<script>
import Pictures from "./Pictures.vue";

export default {
    name: "Info",
    components: {
        Pictures,
    },
    data() {
        return {
            isWorking: false,
            show_Email: true,
            email: "email@email.com.br",
            meuLink: "https://google.com.br",
            buttonEmail: "Mostrar e-mail"
        }
    },
    methods: {
        showEmail() {
            this.show_Email = !this.show_Email
            
            if(!this.show_Email) {
                this.buttonEmail = "Mostrar e-mail"
            } else {
                this.buttonEmail = "Esconder e-mail"
            }
        }
    }
}
</script>

<template>
    <div>
        <!-- Conectados v-if e v-else -->
        <p v-if="isWorking">Trabalhando atualmente</p>
        <p v-else>Procurando emprego</p>
        <p>Conhecimentos em:</p>
        <ul>
            <li>HMTL</li>
            <li>CSS</li>
            <li>JavaScritp</li>
        </ul>
        <button @click="showEmail" class="p-2 bg-green-400 rounded-md cursor-pointer">{{ buttonEmail }}</button>
        <p v-show="show_Email">Mande um email para: {{ email }}</p>
        <!-- Para deixar uma diretiva dinâmica, pode colocar o v-bind:... -->
        <p> Acesso para o meu portiófólio: <a v-bind:href="meuLink" target="_blank">Clique Aqui!</a></p>
        <Pictures />
    </div>
</template>