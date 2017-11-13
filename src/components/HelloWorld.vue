<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>
      <button @click="$toast('toast')">toast</button>
      <button @click="loading">loading</button>
    </h2>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Abandon'
    }
  },
  methods: {
    loading () {
      this.$indicator.open()
      setTimeout(() => {
        this.$indicator.close()
      }, 200)
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
