<template>
    <div>
      <h1>
        Testando o Vuex
      </h1>
      <h4>
        {{user}}
      </h4>
      <hr>
      <c-users></c-users>
    </div>
</template>

<script>
import cUsers from './components/users/main.vue'
export default {
  components: {
    cUsers
  },
  computed: {
    user () {
      const { name, email } = this.$store.state.user
      return `O usuário logado é ${name} e possui o email ${email}.`
    }
  }
}
</script>

<style>

</style>
