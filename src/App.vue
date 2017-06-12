<template>
  <div id="app">
    <img src="./assets/logo.png">
    {{userName}}
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app',
  computed: {
    userName(){
      console.log(this.$store.state)
      return this.$store.state.user.userInfo.name
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
