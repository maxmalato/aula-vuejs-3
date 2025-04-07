<script>
import Pictures from "./Pictures.vue";

export default {
    name: "Info",
    components: {
        Pictures,
    },
    props: {
        compEmail: {
            type: String,
            required: true
        }
    },
    data() {
        return {
            isWorking: false,
            show_Email: true,
            email: "email@email.com.br",
            meuLink: "https://google.com.br",
            buttonEmail: "Mostrar e-mail",
            backendTech: ["PHP", "NodeJS", "C#", "Go", "Python"],
            frontendTech: [
                {id: 1, language: "HTML"},
                {id: 2, language: "CSS"},
                {id: 3, language: "JavaScript"}
            ]
        };
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
        
        <p class="font-semibold text-xl">Conhecimentos em Back-End:</p>
        <ul v-for="tech in backendTech">
            <li>{{ tech }}</li>
        </ul>
        
        <p class="font-semibold text-xl">Conhecimentos em Front-End:</p>
        <ul v-for="tech in frontendTech">
            <li>{{ tech.language }}</li>
        </ul>

        <button @click="showEmail" class="p-2 bg-green-400 rounded-md cursor-pointer">{{ buttonEmail }}</button>
        <p v-show="show_Email">Mande um email para: {{ email }}</p>
        <!-- Para deixar uma diretiva dinâmica, pode colocar o v-bind:... -->
        <p> Acesso para o meu portiófólio: <a v-bind:href="meuLink" target="_blank">Clique Aqui!</a></p>
        <Pictures />
        <p class="font-semibold text-xl">Email do componente: {{ compEmail }}</p>
    </div>
</template>