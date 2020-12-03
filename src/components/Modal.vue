<template>
  <div class="backdrop">
    <div class="modal">
      <h1>Modal Title</h1>
      <p>modal content</p>
    </div>
  </div>
</template>

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
</style>
