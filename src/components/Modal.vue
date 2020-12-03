<template>
  <div class="backdrop" @click.self="closeModal">
    <div class="modal" :class="{ sale: theme === 'sale' }">
      <slot>Default slot</slot>
      <div class="actions">
        <slot name="links"></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['header', 'text', 'theme'],
  methods: {
    closeModal() {
      this.$emit('close');
    },
  },
};
</script>

<style>
.modal {
  width: 400px;
  padding: 20px;
  margin: 100px auto;
  background: #fff;
  border-radius: 10px;
}
.backdrop {
  position: fixed;
  background: rgba(0, 0, 0, 0.5);
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
}
.modal h1 {
  color: #0fb;
  display: inline-block;
}
.modal.sale {
  background: crimson;
  color: #fff;
}
.modal.sale h1 {
  color: #fff;
}
.modal .actions {
  margin: 30px 0 10px 0;
}
.modal .actions a {
  color: #333;
  text-decoration: none;
  padding: 10px;
  margin: 10px;
  border: 1px solid #333;
  border-radius: 4px;
}
.modal.sale .actions a {
  color: #fff;
  border-color: #fff;
}
</style>
