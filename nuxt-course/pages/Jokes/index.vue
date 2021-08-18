<template>
    <div>
      <h1>Jokes</h1>
      <div class="joke">
        <joke v-for="joke in jokes" :key="joke.id" :id="joke.id" :joke="joke.joke" />
      </div>
    </div>
</template>

<script>
import axios from 'axios'
import joke from '../../components/joke.vue'

export default {
  components : { joke },

  head() {
    return {
      title: 'Welcome to Jokes Page',
      meta: [{
        hid: 'description',
        name: 'description',
        content: 'My first nuxt application'
      }]
    }
  },

  data() {
    return {
      jokes: []
    }
  },

  async created() {
    const config = {
      headers: {
        'Accept' : 'application/json'
      }
    }

    try {
      const res = await axios.get('https://icanhazdadjoke.com/search', config)
      this.jokes = res.data.results
    }
    catch (error) {
      console.log(err)
    }
  }
}
</script>

<style>
  .joke {
    padding: 1rem;
    border: 1px dotted #ccc;
    margin: 1rem 0;
  }
</style>
