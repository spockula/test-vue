<template>
  <div class="bg-white px-8 overflow-hidden ">
    <AppHeader />
    <nuxt />
  </div>
</template>

<script lang="ts">
  import Vue from 'vue';
  import AppHeader from '../components/AppHeader.vue';
  export default Vue.extend({
    components: { AppHeader }
})
</script>

<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  body  {
    font-family: Arial, Helvetica, sans-serif;
    font-size: 1rem;
    line-height: 1.6;
    background: white;
  }
</style>
