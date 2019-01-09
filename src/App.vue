<template>
    <div>
      <h1>
        Testando o Vuex
      </h1>
      <h4>
        {{user}} {{outraCoisa}}
      </h4>
      <hr>
      <c-users></c-users>
    </div>
</template>

<script>
import cUsers from './components/users/main.vue'
import { mapState, mapActions } from 'vuex'

export default {
  mounted() {
    const payload = {
      name: 'João Henrique',
      email: 'joao@hotmail.com',
      level: 'admin',
      city: 'Goiânia',
      state: 'GO'
    }

    setTimeout(() => {
      this.changeUser(payload)
    }, 3000)
  },
  components: {
    cUsers
  },
  computed: {
    outraCoisa () {
      return 'Mais uma informação!'
    },
    ...mapState({
      user: state => {
        const { name, email } = state.user
        return `O usuário logado é ${name} e possui o email ${email}.`
      }
    })
  },
  methods: {
    ...mapActions(['changeUser']) // método changeUser passa a ser acessível dentro do component, está mapeado
  }
}
</script>

<style>

</style>
