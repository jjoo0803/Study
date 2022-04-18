<template>
  <div id="app">
    <nav>
      <!-- <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/test">test</router-link> -->
      <button @click="goToHomePage">Home</button> |
      <button @click="goToAboutPage">About</button>
    </nav>
    <router-view />
  </div>
</template>

<script>
export default {
  created () {
    // this.$router.push('/')
  },
  methods: {
    goToHomePage () {
      // this.$router.push('가고 싶은 경로').catch(() => {})
      this.$router.push('/').catch(() => {})
    },
    goToAboutPage () {
      this.$router.push('/about').catch(() => {})
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}


nav {
  padding: 30px;

  button {
    font-weight: bold;
    color: #2c3e50;

    &:active {
      color: #42b983;
    }
  }
}
</style>
