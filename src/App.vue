<template>
  <h1>{{ title }}</h1>
  <input type="text" ref="name" />
  <button @click="handleClick">Click me</button>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      title: 'Welcome to Vue.js',
    };
  },
  methods: {
    handleClick() {
      this.$refs.name.focus();
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1 {
  padding-bottom: 10px;
  border-bottom: 1px solid #ddd;
}
</style>
