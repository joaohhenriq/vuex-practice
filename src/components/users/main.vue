<template>
    <div>
        Email: {{email}}
        <p>Localidade: {{localidade}}</p>
        <c-button></c-button>
    </div>
</template>

<script>
import cButton from '../button.vue'
export default {
    components: {
        cButton
    },
    computed: {
        email () {
            return this.$store.state.user.email
        },
        localidade () {
            return this.$store.getters.localidade
        }
    }
}
</script>

<style>

</style>
