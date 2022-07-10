<template>
  <div>
    <button @click="showModalSlide()">SHOW MODAL SLIDE UP</button>
    <button @click="showNormalModal()" style="background-color: ; margin-left: 40px">SHOW NORMAL MODAL</button>
    <Modal 
      :is-show="isShow"
      @updateIsShow="updateIsShow"
    />
    <NormalModal 
      :is-show-normal="isShowNormal"
      @updateIsShowNormal="updateIsShowNormal"
    />
  </div>
</template>

<script>
import Modal from './components/Modal.vue'
import NormalModal from './components/NormalModal.vue'

export default {
  name: 'App',
  components: {
    Modal,
    NormalModal
  },
  data() {
    return {
      isShow : false,
      isShowNormal: false
    }
  },
  methods : {
    showModalSlide(){
      this.isShow  = true
    },
    showNormalModal() {
      this.isShowNormal  = true
    },
    updateIsShow(value) {
      this.isShow = value
    },
    updateIsShowNormal(value) {
      this.isShowNormal = value
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
