<template>
<div>
  <div v-if="user" class="account">
    HELLO
  </div>
  <not-logged-in v-else />
</div>
</template>

<script>
// @ is an alias to /src
import NotLoggedIn from '@/components/NotLoggedIn.vue'

export default {
  name: 'account',
  components: {
    NotLoggedIn
  },
  computed: {
    user() {
      return this.$store.state.user;
    },
  }
}
</script>

<style scoped>
.center{
  display: block;
  width: 100%; 
  margin: 0 auto;
  text-align: center;
}
.link
{
  text-decoration: none;
  color: black;
}
.sign-in
{
  margin-top: 8%;
  border: 1px solid #ccc;
  background-color: #eee;
  border-radius: 4px;
  padding: 20px;
  color: black;
  width: 30%;
  max-width: 300px;
}
.margin {
  margin-top: 0px;
  margin-bottom: 15px;
}
</style>