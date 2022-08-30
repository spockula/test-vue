  <template>
    <h1 class="mt-2 mx-4"> {{ name }}</h1>
  </template>


  <script lang="ts">
  import Vue from 'vue'
  export default Vue.extend({
    name: 'details',
    data: () => ({
      name: 'chinedu' as string,
    }),
    head() {
      return {
        title: 'About page',
        meta: [
          {
            hid: 'description',
            name: 'about',
            content: 'my about page'
          }
        ]
      }
    }
  })
  </script>
