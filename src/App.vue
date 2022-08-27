<template>
  <div id="flashMessage" v-if="GStore.flashMessage">
    {{ GStore.flashMessage }}
  </div>
  <div id="nav">
    <router-link :to="{ name: 'EventList' }">Home</router-link>&nbsp; |
    &nbsp;<router-link :to="{ name: 'About' }">About</router-link>
  </div>

  <!-- new element -->
  <router-view />
</template>

<script>
export default {
  inject: ['GStore'] // <----
}
</script>
<style>
@keyframes yellowfade {
  from {
    background: yellow;
  }
  to {
    background: transparent;
  }
}

#flashMessage {
  animation-name: yellowfade;
  animation-duration: 3s;
}
#app {
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fcfcfc;
}

#nav {
  padding: 30px;
}

#nav a {
  font-size: 30px;
  word-spacing: 30px;
  font-weight: bold;
  color: #fcfcfc;
}

#nav a.router-link-exact-active {
  color: #e91e63;
}
h4 {
  font-size: 20px;
}

body {
  background-image: url('../src/assets/picback2.jpg');
  background-size: 1600px;
  background-attachment: fixed;
}
</style>
