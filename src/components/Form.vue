<script>
import InputText from "./form/InputText.vue"
import Submit from "./form/Submit.vue"

export default {
    name: "Form",
    components: {
        InputText,
        Submit
    }
}
</script>

<template>
    <div>
        <form action="" class="flex flex-col gap-2">
            <InputText />
            <InputText />
            <Submit />
        </form>
    </div>
</template>