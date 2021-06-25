<template>
  <div class="about">
    <button @click="showModal">open modal</button>
    <Modal v-if="modalVisible" @close="closeModal" @plus="plusCount" />

    <div class="margin-top-20">{{ `count: ${count}` }}</div>
  </div>
</template>

<script>
import Modal from "@/components/Modal.vue";

export default {
  name: "About",
  components: {
    Modal,
  },
  data() {
    return {
      modalVisible: false,
      count: 0,
    };
  },
  created() {},
  methods: {
    showModal() {
      this.modalVisible = true;
    },
    closeModal() {
      this.modalVisible = false;
    },
    plusCount() {
      this.count = this.count + 1;
    },
  },
};
</script>

<style lang="scss">
.margin-top-20 {
  margin-top: 20px;
}
</style>
