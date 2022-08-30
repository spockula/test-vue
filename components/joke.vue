<template>
  <nuxt-link :to="'jokes/' + id"> 
    <div class=" p-4 border-dotted border-[1px] border-gray-300 mt-4 ">
      <p> {{joke}} </p>
    </div>
  </nuxt-link>
</template>

<script lang="ts">
  import Vue from 'vue'
  export default Vue.extend({
    name: 'jokes',
    props: ['joke', 'id']
  })
</script>