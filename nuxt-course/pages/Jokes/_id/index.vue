<template>
  <div>
    <nuxt-link to="/jokes">Back to Jokes: </nuxt-link>
    <h1>{{joke}}</h1>
    <hr />
    <small>Joke id is: {{ $route.params.id }}</small>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  data() {
    return {
      joke: {}
    }
  },

  async created() {
    const config = {
      headers: {
        Accept : 'application/json'
      }
    }

    try {
      const res = await axios.get(`https://icanhazdadjoke.com/j/${this.$route.params.id}`, config)
      this.joke = res.data.joke
      console.log(this.joke)
    } catch (err) {
      console.log(err)
    }
  }
}
</script>

<style>

</style>
