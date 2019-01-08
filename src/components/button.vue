<template>
    <div>
        <button @click="mudarDados">
            Mudar dados do usuário
        </button>
    </div>
</template>

<script>
export default {
    methods: {
        mudarDados () {
            const payload = {
                name: 'Outro nome',
                email: 'outroemail@hotmail.com',
                level: 'outroLevel'
            }

            this.$store.commit('CHANGE_USER', payload)
        }
    }
}
</script>

<style>

</style>
