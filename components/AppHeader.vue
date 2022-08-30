<template>
  <header class="flex justify-between items-center mb-4 py-4 border-b border-dotted ">
    <h1 class=" text-5xl text-gray-400 ">
      Ogu Chinedu
    </h1>
    <ul class="flex">
      <li class=" inline-block bg-slate-700 text-white py-1 px-4 mr-2 ">
        <nuxt-link to="/"> Home </nuxt-link>
      </li>
      <li class=" inline-block bg-slate-700 text-white py-1 px-4 mr-2 ">
        <nuxt-link to="/about"> About </nuxt-link>
      </li>
      <li class=" inline-block bg-slate-700 text-white py-1 px-4 mr-2 ">
        <nuxt-link to="/jokes"> Jokes </nuxt-link>
      </li>
    </ul>
  </header>
</template>

<script lang="ts">
  import Vue from 'vue'
  export default Vue.extend({
    name: 'AppHeader'
  })
</script>
