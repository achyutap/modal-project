<template>
  <div class="back" @click.self="closeModal()">
    <div class="modal">
      <slot></slot>
      <div>
          <slot name="links"></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["title", "desc"],

  methods: {
    showModal() {
      this.modal = !this.modal;
    },
    closeModal() {
      this.$emit("close");
    },
  },
};
</script>

<style>
body,
html {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
}
.back {
  position: fixed;
  display: flex;
  justify-content: center;
  align-items: center;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgb(167, 167, 167);
}
.modal {
  width: 500px;
  height: 200px;
  display: flex;
  justify-content: center;
  flex-direction: column;
  background-color: rgb(194, 74, 74);
}
</style>