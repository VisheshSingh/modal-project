<template>
  <h1>{{ title }}</h1>
  <p>hey peeps!!!</p>
  <div v-if="showModal">
    <Modal :header="header" :text="text" theme="sale" @close="toggleModal" />
  </div>
  <button @click="toggleModal">Open Modal</button>
</template>

<script>
import Modal from './components/Modal';

export default {
  name: 'App',
  components: {
    Modal,
  },
  data() {
    return {
      title: 'Welcome to Vue.js',
      header: 'Signup for the giveaway!',
      text: 'Grab the cool merchandize 🧥 at half the price',
      showModal: false,
    };
  },
  methods: {
    handleClick() {
      this.$refs.name.focus();
    },
    toggleModal() {
      this.showModal = !this.showModal;
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
