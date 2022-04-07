<template>
  <div class="home">
    <img alt="Vue logo" class="photo-small" src="../assets/beauty.jpg">
    <large-container :title="titulary" />
  </div>
</template>

<script>
// @ is an alias to /src
import LargeContainer from '../components/LargeContainer.vue'

export default {
  name: 'Home',
  components: {
    'large-container': LargeContainer
  },

  data () {
    return {
      titulary: 'Here we create new cards'
    }
  }
}
</script>

<style scoped>
  .photo-small {
     width: 20%;
  height: auto;

  }
</style>
