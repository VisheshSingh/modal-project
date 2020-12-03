<template>
  <h1>{{ title }}</h1>
  <p>hey peeps!!!</p>
  <div v-if="showModal">
    <Modal theme="sale" @close="toggleModal">
      <template v-slot:links>
        <a href="#">Sign up</a>
        <a href="#">More info.</a>
      </template>
      <h1>Signup for the giveaway!!!</h1>
      <p>Grab the cool merchandize 🧥 at half the price</p>
    </Modal>
  </div>
  <button @click.alt="toggleModal">Open Modal (alt)</button>
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
