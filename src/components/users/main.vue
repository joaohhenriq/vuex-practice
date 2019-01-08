<template>
    <div>
        Email: {{email}}
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
        }
    }
}
</script>

<style>

</style>
