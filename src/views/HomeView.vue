<template>
  <div class="home">
    <component :is="current"></component>
  </div>
</template>

<script>
import { mapState } from 'vuex'
// @ is an alias to /src
import ContentComponent from '../components/ContentComponent.vue'
import MovieComponent from '../components/MovieComponent.vue'

export default {
  name: 'HomeView',
  components: {
    ContentComponent,
    MovieComponent
  },
  computed: {
    ...mapState(['current'])
  }
}
</script>
