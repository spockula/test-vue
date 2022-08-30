<template>
  <div>
    <h2>Welcome to my portfolio </h2>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'Home',
  head() {
    return {
      title: "Ogu chinedu's portfolio",
      meta: [
        {
          hid: 'description',
          name: 'Ogu chinedu',
          content: 'my portfolio'
        }
      ]
    }
  }
})
</script>
