<template>
    <div >

        <!-- <h1>EXAMPLE!</h1> -->
        <Home />

    </div>
</template>

<script>
import Home from '../../../src/App.vue'
   export default {
  components: {
      Home
  },
  computed: {
    username() {
      // We will see what `params` is shortly
      return this.$route.params.username
    }
  },
  methods: {
    goBack() {
      window.history.length > 1 ? this.$router.go(-1) : this.$router.push('/')
    }
  }
}
</script>
