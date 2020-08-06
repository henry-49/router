<template>
  <div class="profile">
  <h2>Profile Page ( {{ UserId }} ) </h2>
  </div>
</template>

<script>
export default {
  name: 'Profile',
  data () {
    return {
      // parsing paramer to a route
      UserId: this.$route.params.user_id
    }
  },

  methods: {
    updateId(){
      // helps to avoid reloading the page before updates
      this.UserId = this.$route.params.user_id
    }
  },

  watch: {
    // watch out for updates
    $route: 'updateId'
  }


}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h2{
    color:green;
  }

</style>
