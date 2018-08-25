<template>
  <div class="test">
    test
    <button @click="toBack">返回</button>
  </div>
</template>

<script>
export default {
  name: 'Test',
  data () {
    return {
    }
  },
  methods: {
    toBack () {
      this.$store.commit('reduce', 'Test')
      this.$router.push({ name: 'HelloWorld', params: {} })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
