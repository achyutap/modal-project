<template>
  <button @click="showModal" >click</button>
  <button @click="showModalTwo" >click 2</button>
  <div v-if="modal" style="width:100%; height:100%">
    <Modal @close="showModal">
      <template v-slot:links>
        <a href="#">
          fhej
        </a>
      </template>
      <h1>
        hey heyhey heyhey heyhey heyhey heyhey heyhey heyhey heyhey hey
      </h1>
    </Modal>

  </div>
  <div v-if="modal2" style="width:100%; height:100%">
    <Modal @close="showModalTwo">
      <h1>
        gale
      </h1>
    </Modal>
  </div>
</template>

<script>
import Modal from "./components/Modal.vue";

export default {
  name: "App",
  components: {
    Modal
  },
  data() {
    return {
      title: "hey",
      showName: true,
      modal: false,
      modal2: false,
    };
  },
  methods: {
    showModal() {
      this.modal = !this.modal;
    },
    showModalTwo() {
      this.modal2 = !this.modal2;
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
</style>