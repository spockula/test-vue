<template>
  <div>
    <nuxt-link to="/jokes">
      Back to jokes
    </nuxt-link>
    <h2> {{joke}} </h2>
    <hr />
    <small> joke ID: {{$route.params.id}} </small>
  
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import axios from 'axios';

export default Vue.extend({
  data () {
    return {
      joke: {

      },
    }
  },
  async created () {
    const config = {
        headers: {
          'Accept': 'application/json'
        }
      }
      try {
        const response = await axios.get(`https://icanhazdadjoke.com/j/${this.$route.params.id}` , config); 
        this.joke = response.data.joke;
        console.log('response', this.joke)
      } catch (err) {
        console.log(err)
          
      }
  },
   head() {
      return {
        title: 'Joke',
        meta: [
          {
            hid: 'description',
            name: 'about',
            content: 'my about page'
          }
        ]
      }
  },
})
</script>