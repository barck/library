<template>
  <div class="panel-signUp">
    <form>
      <input type="text" id="input-email" v-model="user">
      <button @click.prevent="onSignUp">Зарегестрироваться</button>
    </form>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'HelloWorld',
  data () {
    return {
      user: ''
    }
  },
  methods: {
    onSignUp: function () {
      axios.post('http://localhost:3000/db', {user2: { userID: 2, UserName: 'TTT' }}).then(function (response) {
        console.log(response)
      })
        .catch(function (error) {
          console.log(error)
        })
    }
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
