<template>
  <div class="overlay" :class="isShow ? 'slide': 'close'">
    <div>
        <h1 class="close-btn" @click="close">
            × &nbsp;
        </h1>
    </div>
</div>
</template>

<script>
export default {
  name: 'Modal',
  props: {
    isShow: Boolean
  },
  methods: {
    close() {
      this.$emit('updateIsShow', false)
    }
  },
}
</script>

<style scoped> 
.overlay {
    width: 50%;
    height: 0;
    position: fixed;
    bottom: 0;
    left: 25%;
    z-index: 1;
    background-color: #add8e6;
    overflow-y: hidden;
    transition: 1.0s;
}
.close-btn{
    cursor: pointer;
}
.slide {
  height: 70%;
}
.close {
  height: 0%;
}
</style>
