<template>
    <div>
        <button :disabled="!hasUser" @click="mudarDados">
            Mudar dados do usuário
        </button>
    </div>
</template>

<script>
import { mapActions } from 'vuex'

export default {
    methods: {
        mudarDados () {
            const payload = {
                name: 'Outro nome',
                email: 'outroemail@hotmail.com',
                level: 'outroLevel',
                city: 'Goiânia',
                state: 'GO'
            }

            this.changeUser(payload)
        },
        ...mapActions(['changeUser'])
    },
    computed: {
        hasUser () {
            return this.$store.state.user.name !== ''
        }
    }
}
</script>

<style>

</style>
