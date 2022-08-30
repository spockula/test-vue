<template>
  <div>
    <Search v-on:search-text="searchText" />
    <Joke v-for="joke in jokes" v-bind:key="joke.id" :id="joke.id" :joke="joke.joke" />
  </div>
</template>


 <script lang="ts">
  import Vue from 'vue'
  import axios from 'axios';
  import Joke from '~/components/joke.vue';
  import Search from '~/components/search.vue';

  export default Vue.extend({
    components: {
    Joke,
    Search
},
    data() {
      return {
        jokes: [] as any[]
      }
    },
    async created () {
      const config = {
        headers: {
          'Accept': 'application/json'
        }
      }
      try {
        const response = await axios.get('https://icanhazdadjoke.com/search', config); 
        this.jokes = response.data.results;
        console.log('response', this.jokes)
      } catch (err) {
        console.log(err)
          
      }
    
    },
    methods: {
      async searchText(text: string) { 
        const config = {
          headers: {
            'Accept': 'application/json'
          }
        }
        try {
          const response = await axios.get(`https://icanhazdadjoke.com/search?term=${text}`, config); 
          this.jokes = response.data.results;
          console.log('response', this.jokes)
        } catch (err) {
          console.log(err)
            
        }
      }
    },
    head() {
        return {
          title: 'Jokes page',
          meta: [
            {
              hid: 'description',
              name: 'jokes',
              content: 'some corny jokes page'
            }
          ]
        }
      }
  })
 </script>
