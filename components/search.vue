<template>
  <form @submit.prevent="onSubmit">
    <input type="text" v-model="text" placeholder="Search for jokes">
    <input type="submit" value="Search Jokes">
  </form>
</template>

<script lang="ts">
  import Vue from 'vue'
  export default Vue.extend({
    name: 'SearchJokes',
     data () {
      return {
         text: ''
      }
     },
     methods: {
      onSubmit() {
        this.$emit('search-text', this.text);
        this.text = '';
      }
     }
  })
</script>