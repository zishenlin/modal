<template>
  <div class="modal-view">
    <div class="overlay" @click="closeModal"></div>
    <div class="modal">
      <button class="plus-btn" type="button" @click="plus">+ plus</button>
      <br />
      <button class="close-btn" type="button" @click="closeModal">close</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Modal",
  data() {
    return {};
  },
  methods: {
    closeModal() {
      this.$emit("close", true);
    },
    plus() {
      this.$emit("plus", true);
    },
  },
};
</script>

<style lang="scss">
.modal-view {
  .overlay {
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    position: fixed;
    z-index: 999;
    background-color: rgba(0, 0, 0, 0.8);
  }
  .modal {
    margin: 0 auto;
    width: 300px;
    height: 300px;
    position: relative;
    z-index: 1000;
    padding: 30px;
    background-color: #fff;
    .close-btn,
    .plus-btn {
      margin: 30px auto 0;
    }
  }
}
</style>
