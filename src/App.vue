<template>
  <div>
    <button @click="showModal()">SHOW MODAL</button>
    <Modal 
    :is-show="isShow"
    @updateIsShow="updateIsShow"
  />
  </div>
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: {
    Modal
  },
  data() {
    return {
      isShow : false
    }
  },
  methods : {
    showModal(){
      this.isShow  = true
    },
    updateIsShow(value) {
      this.isShow = value
    }
  }
}
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
