<script>
export default {
    name: "Pictures",
    data() {
        return {
            avatar: "/favicon.ico",
            description: "VueJS"
        }
    }
}
</script>

<template>
    <img :src="avatar" :alt="description">
</template>
