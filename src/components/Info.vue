<script>
export default {
    name: "Info",
    data() {
        return {
            isWorking: false,
            showEmail: true,
            email: "email@email.com.br"
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
        <p v-show="showEmail">Mande um email para: {{ email }}</p>
    </div>
</template>