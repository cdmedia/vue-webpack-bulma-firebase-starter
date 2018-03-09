<template>
  <div class="container main">
    <h2 class="title is-2">Protected Area</h2>

    <p>This is a place where we can put important things</p>

    <hr>

    <a class="button" @click="logout">Logout</a>

  </div>
</template>

<script>
import firebase from 'firebase';

export default {
  name: 'Protected',
  data() {
    return {
      data: '',
    };
  },
  methods: {
    logout() {
      firebase.auth().signOut().then(() => {
        this.$router.replace('login');
        this.$toast.open({
          message: 'Successfully logged out!',
          position: 'is-bottom',
          type: 'is-success',
        });
      });
    },
  },
};
</script>

<style scoped>
.main {
  margin: 2rem;
}
</style>
