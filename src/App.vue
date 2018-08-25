<template>
  <div id="app">
    <transition name="fade" mode="out-in">
      <keep-alive :include="pages">
        <router-view/>
      </keep-alive>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'App',
  computed: {
    pages () {
      return this.$store.state.pages
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
